---
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611842"
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







# <span data-ttu-id="98d32-103">Справочник по анализу сети</span><span class="sxs-lookup"><span data-stu-id="98d32-103">Network Analysis Reference</span></span>   



<span data-ttu-id="98d32-104">Ознакомьтесь с новыми способами для анализа того, как страница загружается в этой полной версии справочника по функциям сетевого анализа Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="98d32-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="98d32-105">Запись сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-105">Record network requests</span></span>   

<span data-ttu-id="98d32-106">По умолчанию DevTools записывает все сетевые запросы на панели "сеть", пока не откроете DevTools.</span><span class="sxs-lookup"><span data-stu-id="98d32-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

> ##### <span data-ttu-id="98d32-107">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="98d32-107">Figure 1</span></span>  
> <span data-ttu-id="98d32-108">Панель "сеть"</span><span class="sxs-lookup"><span data-stu-id="98d32-108">The Network panel</span></span>  
> ![Панель "сеть"][ImageNetworkPanel]  

### <span data-ttu-id="98d32-110">Прекращение записи сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-110">Stop recording network requests</span></span>   

<span data-ttu-id="98d32-111">Чтобы остановить запись запросов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-111">To stop recording requests:</span></span>  

*   <span data-ttu-id="98d32-112">Выберите **остановить запись** остановка записи сетевого журнала ![ ][ImageRecordOnIcon] на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="98d32-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="98d32-113">Оно превращается в серый, чтобы показать, что DevTools больше не записывает запросы.</span><span class="sxs-lookup"><span data-stu-id="98d32-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
*   <span data-ttu-id="98d32-114">Нажимайте клавиши `Control` + `E` \ (Windows \) или `Command` + `E` \ (macOS \), пока фокус находится на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="98d32-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="98d32-115">Очистка запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-115">Clear requests</span></span>   

<span data-ttu-id="98d32-116">**Clear** ![ ][ImageClearIcon] Чтобы очистить все запросы из таблицы "запросы", на панели "сеть" нажмите кнопку Clear Clear.</span><span class="sxs-lookup"><span data-stu-id="98d32-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

> ##### <span data-ttu-id="98d32-117">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="98d32-117">Figure 2</span></span>  
> <span data-ttu-id="98d32-118">Кнопка "очистить"</span><span class="sxs-lookup"><span data-stu-id="98d32-118">The Clear button</span></span>  
> ![Кнопка "очистить"][ImageClearButton]  

### <span data-ttu-id="98d32-120">Сохранение запросов на загрузку страниц</span><span class="sxs-lookup"><span data-stu-id="98d32-120">Save requests across page loads</span></span>   

<span data-ttu-id="98d32-121">Для сохранения запросов на страницах загрузок на панели "сеть" установите флажок **сохранить журнал** .</span><span class="sxs-lookup"><span data-stu-id="98d32-121">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="98d32-122">DevTools сохраняет все запросы, пока не отключайте параметр **сохранить журнал**.</span><span class="sxs-lookup"><span data-stu-id="98d32-122">DevTools saves all requests until you disable **Preserve log**.</span></span>  

> ##### <span data-ttu-id="98d32-123">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="98d32-123">Figure 3</span></span>  
> <span data-ttu-id="98d32-124">Флажок "сохранить журнал"</span><span class="sxs-lookup"><span data-stu-id="98d32-124">The Preserve Log checkbox</span></span>  
> ![Флажок "сохранить журнал"][ImagePreserveLogCheckBox]  

### <span data-ttu-id="98d32-126">Захват снимков экрана при загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="98d32-126">Capture screenshots during page load</span></span>   

<span data-ttu-id="98d32-127">Выведите снимки экрана, чтобы проанализировать, какие пользователи видят при ожидании загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="98d32-127">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="98d32-128">Чтобы включить снимки экрана, нажмите кнопку **Параметры сети** и выберите команду **захватить снимки экрана** на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="98d32-128">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="98d32-129">Перезагрузите страницу, когда фокус находится на панели " **сеть** ", чтобы захватить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="98d32-129">Reload the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="98d32-130">После захвата снимка экрана вы взаимодействуете с ним следующими способами.</span><span class="sxs-lookup"><span data-stu-id="98d32-130">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="98d32-131">Наведите указатель мыши на снимок экрана, чтобы просмотреть точку, в которой был записан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="98d32-131">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="98d32-132">На панели **обзора** появится желтая линия.</span><span class="sxs-lookup"><span data-stu-id="98d32-132">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="98d32-133">Щелкните эскиз экрана, чтобы отфильтровать все запросы, произошедшие после захвата снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="98d32-133">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="98d32-134">Дважды щелкните эскиз, чтобы увеличить его.</span><span class="sxs-lookup"><span data-stu-id="98d32-134">Double-click a thumbnail to zoom in on it.</span></span>  

> ##### <span data-ttu-id="98d32-135">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="98d32-135">Figure 4</span></span>  
> <span data-ttu-id="98d32-136">Наведение указателя на снимок экрана</span><span class="sxs-lookup"><span data-stu-id="98d32-136">Hovering over a screenshot</span></span>  
> ![Наведение указателя на снимок экрана][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## <span data-ttu-id="98d32-138">Изменение поведения при загрузке</span><span class="sxs-lookup"><span data-stu-id="98d32-138">Change loading behavior</span></span>  

### <span data-ttu-id="98d32-139">Эмуляция первого времени посетителя с помощью отключения кэша браузера</span><span class="sxs-lookup"><span data-stu-id="98d32-139">Emulate a first-time visitor by disabling the browser cache</span></span>   

<span data-ttu-id="98d32-140">Чтобы эмулировать, как пользователь попытается получить доступ к сайту, установите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="98d32-140">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="98d32-141">DevTools отключает кэш браузера.</span><span class="sxs-lookup"><span data-stu-id="98d32-141">DevTools disables the browser cache.</span></span>  <span data-ttu-id="98d32-142">Это более точно эмулирует взаимодействие с пользователем при первом запуске, так как запросы размещаются из кэша браузера на повторных посещениях.</span><span class="sxs-lookup"><span data-stu-id="98d32-142">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

> ##### <span data-ttu-id="98d32-143">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="98d32-143">Figure 5</span></span>  
> <span data-ttu-id="98d32-144">Флажок "отключить кэш"</span><span class="sxs-lookup"><span data-stu-id="98d32-144">The Disable Cache checkbox</span></span>  
> <span data-ttu-id="98d32-145">! [Флажок отключения кэша] [ImageDisableCacheCheckBox]</span><span class="sxs-lookup"><span data-stu-id="98d32-145">![The Disable Cache checkbox][ImageDisableCacheCheckBox]</span></span>  

#### <span data-ttu-id="98d32-146">Отключение кэша браузера из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="98d32-146">Disable the browser cache from the Network Conditions drawer</span></span>   

<span data-ttu-id="98d32-147">Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте денежные ящики условия сети.</span><span class="sxs-lookup"><span data-stu-id="98d32-147">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="98d32-148">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="98d32-148">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="98d32-149">Установите или снимите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="98d32-149">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="98d32-150">Очистка кэша браузера вручную</span><span class="sxs-lookup"><span data-stu-id="98d32-150">Manually clear the browser cache</span></span>   

<span data-ttu-id="98d32-151">Чтобы вручную очистить кэш браузера в любое время, щелкните правой кнопкой мыши в любом месте таблицы запросы и выберите пункт **очистить кэш браузера**.</span><span class="sxs-lookup"><span data-stu-id="98d32-151">To manually clear the browser cache at any time, right-click anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

> ##### <span data-ttu-id="98d32-152">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="98d32-152">Figure 6</span></span>  
> <span data-ttu-id="98d32-153">Выбор очистки кэша браузера</span><span class="sxs-lookup"><span data-stu-id="98d32-153">Selecting Clear Browser Cache</span></span>  
> <span data-ttu-id="98d32-154">! [Выбор очистки кэша браузеров] [ImageClearBrowserCache]</span><span class="sxs-lookup"><span data-stu-id="98d32-154">![Selecting Clear Browser Cache][ImageClearBrowserCache]</span></span>  

### <span data-ttu-id="98d32-155">Эмуляция в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="98d32-155">Emulate offline</span></span>   

<span data-ttu-id="98d32-156">Новый класс веб-приложений, называемый [прогрессивными веб-приложениями][DevtoolsProgressiveWebApps], не будет работать в автономном режиме с помощью **обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="98d32-156">A new class of web apps, called [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="98d32-157">Возможно, вам будет удобно быстро смоделировать устройство, которое не имеет подключения к данным, при построении такого типа приложения.</span><span class="sxs-lookup"><span data-stu-id="98d32-157">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="98d32-158">Щелкните раскрывающееся меню **онлайн** , выполните поиск в разделе " **стили**", а затем выберите пункт в **автономном режиме** , чтобы имитировать полностью автономный режим работы сети.</span><span class="sxs-lookup"><span data-stu-id="98d32-158">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

> ##### <span data-ttu-id="98d32-159">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="98d32-159">Figure 7</span></span>  
> <span data-ttu-id="98d32-160">Раскрывающееся меню "автономный режим"</span><span class="sxs-lookup"><span data-stu-id="98d32-160">The Offline dropdown menu</span></span>  
> <span data-ttu-id="98d32-161">! [Раскрывающееся меню "вне сети"] [ImageOfflineDropdown]</span><span class="sxs-lookup"><span data-stu-id="98d32-161">![The Offline dropdown menu][ImageOfflineDropdown]</span></span>  

### <span data-ttu-id="98d32-162">Эмуляция медленных сетевых подключений</span><span class="sxs-lookup"><span data-stu-id="98d32-162">Emulate slow network connections</span></span>   

<span data-ttu-id="98d32-163">Эмуляция медленной сети 3G, Fast 3G и других скоростей соединения из раскрывающегося меню **Online** .</span><span class="sxs-lookup"><span data-stu-id="98d32-163">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

> ##### <span data-ttu-id="98d32-164">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="98d32-164">Figure 8</span></span>  
> <span data-ttu-id="98d32-165">Раскрывающееся меню регулирования</span><span class="sxs-lookup"><span data-stu-id="98d32-165">The Throttling dropdown menu</span></span>  
> <span data-ttu-id="98d32-166">! [Раскрывающееся меню регулирования] [ImageNetworkThrottlingMenu]</span><span class="sxs-lookup"><span data-stu-id="98d32-166">![The Throttling dropdown menu][ImageNetworkThrottlingMenu]</span></span>  

<span data-ttu-id="98d32-167">Вы можете выбрать один из самых разнообразных наборов параметров, например медленной или скорости 3G.</span><span class="sxs-lookup"><span data-stu-id="98d32-167">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="98d32-168">Вы также можете добавить собственные пользовательские стили, открыв меню регулирования и выбрав пункт **настраиваемое**  >  **Добавление**.</span><span class="sxs-lookup"><span data-stu-id="98d32-168">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="98d32-169">DevTools отображает значок предупреждения рядом с вкладкой **сеть** , чтобы напомнить вам, что регулирование разрешено.</span><span class="sxs-lookup"><span data-stu-id="98d32-169">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="98d32-170">Эмуляция медленных сетевых подключений из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="98d32-170">Emulate slow network connections from the Network Conditions drawer</span></span>   

<span data-ttu-id="98d32-171">Если вы хотите регулировать сетевое соединение при работе с другими панелями DevTools, используйте денежные ящики условий сети.</span><span class="sxs-lookup"><span data-stu-id="98d32-171">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="98d32-172">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="98d32-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="98d32-173">Выберите нужную скорость соединения в меню **регулирования** .</span><span class="sxs-lookup"><span data-stu-id="98d32-173">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="98d32-174">Очистка файлов cookie браузера вручную</span><span class="sxs-lookup"><span data-stu-id="98d32-174">Manually clear browser cookies</span></span>   

<span data-ttu-id="98d32-175">Чтобы вручную очистить cookie-файлы браузера в любое время, щелкните правой кнопкой мыши в любом месте таблицы запросы и выберите команду **Удалить cookie-файлы браузера**.</span><span class="sxs-lookup"><span data-stu-id="98d32-175">To manually clear browser cookies at any time, right-click anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

> ##### <span data-ttu-id="98d32-176">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="98d32-176">Figure 9</span></span>  
> <span data-ttu-id="98d32-177">Выбор очистки cookie-файлов браузера</span><span class="sxs-lookup"><span data-stu-id="98d32-177">Selecting Clear Browser Cookies</span></span>  
> <span data-ttu-id="98d32-178">! [Выбор очистки cookie-файлов браузера] [ImageClearBrowserCookies]</span><span class="sxs-lookup"><span data-stu-id="98d32-178">![Selecting Clear Browser Cookies][ImageClearBrowserCookies]</span></span>  

### <span data-ttu-id="98d32-179">Переопределение агента пользователя</span><span class="sxs-lookup"><span data-stu-id="98d32-179">Override the user agent</span></span>   

<span data-ttu-id="98d32-180">Чтобы вручную переопределить агент пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-180">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="98d32-181">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="98d32-181">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="98d32-182">Снимите флажок **автоматически**.</span><span class="sxs-lookup"><span data-stu-id="98d32-182">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="98d32-183">Выберите в меню пункт агента пользователя или введите его в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="98d32-183">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="98d32-184">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-184">Filter requests</span></span>   

### <span data-ttu-id="98d32-185">Фильтрация запросов по свойствам</span><span class="sxs-lookup"><span data-stu-id="98d32-185">Filter requests by properties</span></span>   

<span data-ttu-id="98d32-186">С помощью текстового поля **Фильтр** можно отфильтровать запросы по свойствам, таким как домен или размер запроса.</span><span class="sxs-lookup"><span data-stu-id="98d32-186">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="98d32-187">Если надпись не отображается, возможно, область Фильтры скрыта.</span><span class="sxs-lookup"><span data-stu-id="98d32-187">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="98d32-188">Посмотрите [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="98d32-188">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

> ##### <span data-ttu-id="98d32-189">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="98d32-189">Figure 10</span></span>  
> <span data-ttu-id="98d32-190">Текстовое поле "фильтры"</span><span class="sxs-lookup"><span data-stu-id="98d32-190">The Filters text box</span></span>  
> <span data-ttu-id="98d32-191">! [Текстовое поле "фильтры"] [ImageFilterTextBox]</span><span class="sxs-lookup"><span data-stu-id="98d32-191">![The Filters text box][ImageFilterTextBox]</span></span>  

<span data-ttu-id="98d32-192">Вы можете использовать несколько свойств одновременно, разделяя каждое свойство пробелами.</span><span class="sxs-lookup"><span data-stu-id="98d32-192">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="98d32-193">Например, `mime-type:image/png larger-than:1K` отображает все PNGs, размер которых больше 1 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="98d32-193">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="98d32-194">Эти фильтры с несколькими свойствами эквивалентны `AND` операциям.</span><span class="sxs-lookup"><span data-stu-id="98d32-194">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="98d32-195">операции в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="98d32-195">operations are currently not supported.</span></span>  

<span data-ttu-id="98d32-196">Полный список поддерживаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="98d32-196">The complete list of supported properties.</span></span>  

| <span data-ttu-id="98d32-197">Свойство</span><span class="sxs-lookup"><span data-stu-id="98d32-197">Property</span></span> | <span data-ttu-id="98d32-198">Сведения</span><span class="sxs-lookup"><span data-stu-id="98d32-198">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="98d32-199">Отображать только ресурсы из указанного домена.</span><span class="sxs-lookup"><span data-stu-id="98d32-199">Only display resources from the specified domain.</span></span>  <span data-ttu-id="98d32-200">Вы можете использовать подстановочный знак "\ `*` ", чтобы включить несколько доменов.</span><span class="sxs-lookup"><span data-stu-id="98d32-200">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="98d32-201">Например, `*.com` отображаются ресурсы из всех доменных имен, которые заканчиваются на `.com` .</span><span class="sxs-lookup"><span data-stu-id="98d32-201">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="98d32-202">DevTools заполняет раскрывающееся меню автозаполнения всеми найденными доменами.</span><span class="sxs-lookup"><span data-stu-id="98d32-202">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="98d32-203">Показать ресурсы, содержащие указанный заголовок HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="98d32-203">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="98d32-204">DevTools заполняет раскрывающийся список автозавершения всеми найденными заголовками ответов.</span><span class="sxs-lookup"><span data-stu-id="98d32-204">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="98d32-205">Используется `is:running` для поиска `WebSocket` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98d32-205">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="98d32-206">Показать ресурсы, размер которых больше указанного (в байтах).</span><span class="sxs-lookup"><span data-stu-id="98d32-206">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="98d32-207">Установка значения эквивалентно значению свойства `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="98d32-207">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="98d32-208">Показать ресурсы, полученные с помощью указанного типа метода HTTP.</span><span class="sxs-lookup"><span data-stu-id="98d32-208">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="98d32-209">DevTools заполнит раскрывающийся список всех обнаруженных методов HTTP.</span><span class="sxs-lookup"><span data-stu-id="98d32-209">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="98d32-210">Показать ресурсы указанного типа MIME.</span><span class="sxs-lookup"><span data-stu-id="98d32-210">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="98d32-211">DevTools наполняет в раскрывающемся списке все обнаруженные типы MIME.</span><span class="sxs-lookup"><span data-stu-id="98d32-211">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="98d32-212">Показать все смешанные ресурсы контента \ ( `mixed-content:all` \) или только те из них, которые в данный момент отображаются \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="98d32-212">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="98d32-213">Показать ресурсы, полученные через незащищенные HTTP \ ( `scheme:http` \) или защищенные HTTPS \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="98d32-213">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="98d32-214">Показать ресурсы с `Set-Cookie` заголовком с `Domain` атрибутом, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="98d32-214">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="98d32-215">DevTools заполняет Автозаполнение всеми обнаруженными ими доменами cookie.</span><span class="sxs-lookup"><span data-stu-id="98d32-215">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="98d32-216">Показать ресурсы с `Set-Cookie` заголовком с именем, которое соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="98d32-216">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="98d32-217">DevTools заполняет Автозаполнение всеми именами cookie-файлов, которые были обнаружены.</span><span class="sxs-lookup"><span data-stu-id="98d32-217">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="98d32-218">Показать ресурсы с `Set-Cookie` заголовком со значением, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="98d32-218">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="98d32-219">DevTools заполняет Автозаполнение всеми обнаруженными значениями cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="98d32-219">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="98d32-220">Показать только ресурсы, для которых код состояния HTTP соответствует указанному коду.</span><span class="sxs-lookup"><span data-stu-id="98d32-220">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="98d32-221">DevTools заполнит раскрывающееся меню автозаполнения, содержащее все найденные коды состояния.</span><span class="sxs-lookup"><span data-stu-id="98d32-221">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="98d32-222">Фильтрация запросов по типу</span><span class="sxs-lookup"><span data-stu-id="98d32-222">Filter requests by type</span></span>   

<span data-ttu-id="98d32-223">Чтобы отфильтровать запросы по типу запроса, выберите один из указанных ниже кнопок: **XHR**, **JS**, **CSS**, **img**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Манифест**или **другой** \ (любой другой тип, не указанный здесь) на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="98d32-223">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="98d32-224">Если эти кнопки не отображаются, возможно, область фильтров скрыта.</span><span class="sxs-lookup"><span data-stu-id="98d32-224">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="98d32-225">Посмотрите [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="98d32-225">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="98d32-226">Чтобы включить множественные фильтры типов одновременно, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и выберите.</span><span class="sxs-lookup"><span data-stu-id="98d32-226">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

> ##### <span data-ttu-id="98d32-227">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="98d32-227">Figure 11</span></span>  
> <span data-ttu-id="98d32-228">Использование фильтров типов для отображения ресурсов JS, CSS и документов</span><span class="sxs-lookup"><span data-stu-id="98d32-228">Using the Type filters to display JS, CSS, and Document resources</span></span>  
> <span data-ttu-id="98d32-229">! [Использование фильтров типов для отображения ресурсов JS, CSS и документов] [ImageMultiTypeFilter]</span><span class="sxs-lookup"><span data-stu-id="98d32-229">![Using the Type filters to display JS, CSS, and Document resources][ImageMultiTypeFilter]</span></span>  

### <span data-ttu-id="98d32-230">Фильтрация запросов по времени</span><span class="sxs-lookup"><span data-stu-id="98d32-230">Filter requests by time</span></span>   

<span data-ttu-id="98d32-231">Чтобы отобразить только те запросы, которые были активны в течение этого времени, выберите и перетащите его влево или вправо в области "Обзор".</span><span class="sxs-lookup"><span data-stu-id="98d32-231">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="98d32-232">Фильтр является инклюзивным.</span><span class="sxs-lookup"><span data-stu-id="98d32-232">The filter is inclusive.</span></span>  <span data-ttu-id="98d32-233">Отображается любой запрос, который был активен в течение выбранного периода времени.</span><span class="sxs-lookup"><span data-stu-id="98d32-233">Any request that was active during the highlighted time is shown.</span></span>  

> ##### <span data-ttu-id="98d32-234">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="98d32-234">Figure 12</span></span>  
> <span data-ttu-id="98d32-235">Фильтрация запросов, которые неактивны вокруг 300ms</span><span class="sxs-lookup"><span data-stu-id="98d32-235">Filtering out any requests that were inactive around 300ms</span></span>  
> <span data-ttu-id="98d32-236">! [Фильтрация запросов, которые неактивны вокруг 300ms] [ImageOverviewFilter]</span><span class="sxs-lookup"><span data-stu-id="98d32-236">![Filtering out any requests that were inactive around 300ms][ImageOverviewFilter]</span></span>  

### <span data-ttu-id="98d32-237">Скрыть URL-адреса данных</span><span class="sxs-lookup"><span data-stu-id="98d32-237">Hide data URLs</span></span>  

<span data-ttu-id="98d32-238">[URL-адреса данных][MDNHTTPDataURIs] — это небольшие файлы, внедренные в другие документы.</span><span class="sxs-lookup"><span data-stu-id="98d32-238">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="98d32-239">Любой запрос, который начинается с адреса в таблице запросов, `data:` — это URL-адрес данных.</span><span class="sxs-lookup"><span data-stu-id="98d32-239">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="98d32-240">Установите флажок **скрыть URL-адреса данных** , чтобы скрыть эти запросы.</span><span class="sxs-lookup"><span data-stu-id="98d32-240">Check the **Hide data URLs** checkbox to hide these requests.</span></span>  

> ##### <span data-ttu-id="98d32-241">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="98d32-241">Figure 13</span></span>  
> <span data-ttu-id="98d32-242">Флажок "скрыть URL-адреса данных"</span><span class="sxs-lookup"><span data-stu-id="98d32-242">The Hide Data URLs checkbox</span></span>  
> <span data-ttu-id="98d32-243">! [Флажок "скрыть URL-адреса данных]" [ImageHideDataURLsCheckBox]</span><span class="sxs-lookup"><span data-stu-id="98d32-243">![The Hide Data URLs checkbox][ImageHideDataURLsCheckBox]</span></span>  

## <span data-ttu-id="98d32-244">Запросы сортировки</span><span class="sxs-lookup"><span data-stu-id="98d32-244">Sort requests</span></span>  

<span data-ttu-id="98d32-245">По умолчанию запросы в таблице запросов сортируются по времени запуска, но вы можете отсортировать таблицу с помощью других условий.</span><span class="sxs-lookup"><span data-stu-id="98d32-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="98d32-246">Сортировка по столбцам</span><span class="sxs-lookup"><span data-stu-id="98d32-246">Sort by column</span></span>   

<span data-ttu-id="98d32-247">Выберите верхний колонтитул любого столбца в списке запросы для сортировки запросов по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="98d32-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="98d32-248">Этап сортировки по действию</span><span class="sxs-lookup"><span data-stu-id="98d32-248">Sort by activity phase</span></span>   

<span data-ttu-id="98d32-249">Чтобы изменить способ сортировки запросов каскадом, щелкните правой кнопкой мыши заголовок таблицы запросы, наведите указатель на пункт **Каскад**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="98d32-249">To change how the Waterfall sorts requests, right-click the header of the Requests table, hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="98d32-250">**Время начала**.</span><span class="sxs-lookup"><span data-stu-id="98d32-250">**Start Time**.</span></span>  <span data-ttu-id="98d32-251">Первый инициированный запрос находится наверху.</span><span class="sxs-lookup"><span data-stu-id="98d32-251">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="98d32-252">**Время отклика**.</span><span class="sxs-lookup"><span data-stu-id="98d32-252">**Response Time**.</span></span>  <span data-ttu-id="98d32-253">Первый запрос, загруженный в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="98d32-253">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="98d32-254">**Время окончания**.</span><span class="sxs-lookup"><span data-stu-id="98d32-254">**End Time**.</span></span>  <span data-ttu-id="98d32-255">Первый завершенный запрос вверху.</span><span class="sxs-lookup"><span data-stu-id="98d32-255">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="98d32-256">**Общая длительность**.</span><span class="sxs-lookup"><span data-stu-id="98d32-256">**Total Duration**.</span></span>  <span data-ttu-id="98d32-257">Запрос с наиболее короткой установкой подключения и запросом и ответом в начале.</span><span class="sxs-lookup"><span data-stu-id="98d32-257">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="98d32-258">**Задержка**.</span><span class="sxs-lookup"><span data-stu-id="98d32-258">**Latency**.</span></span>  <span data-ttu-id="98d32-259">Запрос, который ожидает наиболее короткий момент ответа, находится наверху.</span><span class="sxs-lookup"><span data-stu-id="98d32-259">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="98d32-260">В этих описаниях предполагается, что каждый из вариантов имеет приоритет от кратчайшего к наиболее продолжительному.</span><span class="sxs-lookup"><span data-stu-id="98d32-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="98d32-261">Если выбрать верхний колонтитул столбца **каскадом** , порядок будет изменен на противоположный.</span><span class="sxs-lookup"><span data-stu-id="98d32-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

> ##### <span data-ttu-id="98d32-262">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="98d32-262">Figure 14</span></span>  
> <span data-ttu-id="98d32-263">Сортировка каскадом по общей длительности \ (светлая часть каждого элемента диаграммы затратила время ожидания, а темная часть — это время, затраченное на загрузку байтов)</span><span class="sxs-lookup"><span data-stu-id="98d32-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
> <span data-ttu-id="98d32-264">! [Сортировка каскадом по общей длительности] [ImageWaterfallTotalDuration]</span><span class="sxs-lookup"><span data-stu-id="98d32-264">![Sorting the Waterfall by total duration][ImageWaterfallTotalDuration]</span></span>  

## <span data-ttu-id="98d32-265">Анализ запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-265">Analyze requests</span></span>   

<span data-ttu-id="98d32-266">Пока открыто окно DevTools, все запросы будут регистрироваться на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="98d32-266">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="98d32-267">Проанализируйте запросы с помощью панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="98d32-267">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="98d32-268">Просмотр журнала запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-268">View a log of requests</span></span>   

<span data-ttu-id="98d32-269">С помощью таблицы запросы можно просмотреть журнал всех запросов, выполненных, когда DevTools открыт.</span><span class="sxs-lookup"><span data-stu-id="98d32-269">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="98d32-270">При выборе или наведении указателя мыши на запросы открывается больше сведений о каждом элементе.</span><span class="sxs-lookup"><span data-stu-id="98d32-270">Selecting or hovering over requests reveals more information about each item.</span></span>  

> ##### <span data-ttu-id="98d32-271">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="98d32-271">Figure 15</span></span>  
> <span data-ttu-id="98d32-272">Таблица запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-272">The Requests table</span></span>  
> <span data-ttu-id="98d32-273">! [Таблица запросов] [ImageRequestsTable]</span><span class="sxs-lookup"><span data-stu-id="98d32-273">![The Requests table][ImageRequestsTable]</span></span>  

<span data-ttu-id="98d32-274">По умолчанию в таблице запросов отображаются следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="98d32-274">The Requests table displays the following columns by default:</span></span>  

*   <span data-ttu-id="98d32-275">**Имя**.</span><span class="sxs-lookup"><span data-stu-id="98d32-275">**Name**.</span></span>  <span data-ttu-id="98d32-276">Имя или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="98d32-276">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="98d32-277">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="98d32-277">**Status**.</span></span>  <span data-ttu-id="98d32-278">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="98d32-278">The HTTP status code.</span></span>  
*   <span data-ttu-id="98d32-279">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="98d32-279">**Type**.</span></span>  <span data-ttu-id="98d32-280">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="98d32-280">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="98d32-281">**Инициатор**.</span><span class="sxs-lookup"><span data-stu-id="98d32-281">**Initiator**.</span></span>  <span data-ttu-id="98d32-282">Следующие объекты или процессы инициируют запросы:</span><span class="sxs-lookup"><span data-stu-id="98d32-282">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="98d32-283">**Средство синтаксического анализа**.</span><span class="sxs-lookup"><span data-stu-id="98d32-283">**Parser**.</span></span>  <span data-ttu-id="98d32-284">Средство синтаксического анализа HTML для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="98d32-284">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="98d32-285">**Redirect (перенаправление**).</span><span class="sxs-lookup"><span data-stu-id="98d32-285">**Redirect**.</span></span>  <span data-ttu-id="98d32-286">Переадресация HTTP.</span><span class="sxs-lookup"><span data-stu-id="98d32-286">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="98d32-287">**Сценарий**.</span><span class="sxs-lookup"><span data-stu-id="98d32-287">**Script**.</span></span>  <span data-ttu-id="98d32-288">Функция JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98d32-288">A JavaScript function.</span></span>  
    *   <span data-ttu-id="98d32-289">**Другие**.</span><span class="sxs-lookup"><span data-stu-id="98d32-289">**Other**.</span></span>  <span data-ttu-id="98d32-290">Другие процессы или действия, например переход на страницу с помощью ссылки или ввод URL-адреса в адресную строку.</span><span class="sxs-lookup"><span data-stu-id="98d32-290">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="98d32-291">**Размер**.</span><span class="sxs-lookup"><span data-stu-id="98d32-291">**Size**.</span></span>  <span data-ttu-id="98d32-292">Объединенный размер заголовков ответа и текст ответа, доставленный сервером.</span><span class="sxs-lookup"><span data-stu-id="98d32-292">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="98d32-293">**Time (время**).</span><span class="sxs-lookup"><span data-stu-id="98d32-293">**Time**.</span></span>  <span data-ttu-id="98d32-294">Общая продолжительность от начала запроса до получения последнего байта в ответе.</span><span class="sxs-lookup"><span data-stu-id="98d32-294">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="98d32-295">[**Каскадом**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="98d32-295">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="98d32-296">Визуальная декомпозиция мероприятия для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="98d32-296">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="98d32-297">Добавление и удаление столбцов</span><span class="sxs-lookup"><span data-stu-id="98d32-297">Add or remove columns</span></span>   

<span data-ttu-id="98d32-298">Щелкните правой кнопкой мыши заголовок таблицы запросов и выберите пункт, чтобы скрыть или отобразить ее.</span><span class="sxs-lookup"><span data-stu-id="98d32-298">Right-click the header of the Requests table and select an option to hide or show it.</span></span>  <span data-ttu-id="98d32-299">Параметры, отображаемые в данный момент, отмечены флажками рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="98d32-299">Currently displayed options have checkmarks next to each item.</span></span>  

> ##### <span data-ttu-id="98d32-300">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="98d32-300">Figure 16</span></span>  
> <span data-ttu-id="98d32-301">Добавление столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="98d32-301">Adding a column to the Requests table</span></span>  
> <span data-ttu-id="98d32-302">! [Добавление столбца в таблицу "запросы"] [ImageRequestsTableAddColumn]</span><span class="sxs-lookup"><span data-stu-id="98d32-302">![Adding a column to the Requests table][ImageRequestsTableAddColumn]</span></span>  

#### <span data-ttu-id="98d32-303">Добавление настраиваемых столбцов</span><span class="sxs-lookup"><span data-stu-id="98d32-303">Add custom columns</span></span>   

<span data-ttu-id="98d32-304">Чтобы добавить в таблицу запросов настраиваемый столбец, щелкните правой кнопкой мыши заголовок таблицы запросов и выберите **заголовки ответа**  >  .**Управление столбцами заголовков**.</span><span class="sxs-lookup"><span data-stu-id="98d32-304">To add a custom column to the Requests table, right-click the header of the Requests table and select **Response Headers** > **Manage Header Columns**.</span></span>  

> ##### <span data-ttu-id="98d32-305">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="98d32-305">Figure 17</span></span>  
> <span data-ttu-id="98d32-306">Добавление настраиваемого столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="98d32-306">Adding a custom column to the Requests table</span></span>  
> <span data-ttu-id="98d32-307">! [Добавление настраиваемого столбца в таблицу "запросы"] [ImageRequestsTableCustomColumn]</span><span class="sxs-lookup"><span data-stu-id="98d32-307">![Adding a custom column to the Requests table][ImageRequestsTableCustomColumn]</span></span>  

### <span data-ttu-id="98d32-308">Просмотр времени связи между запросами друг на друга</span><span class="sxs-lookup"><span data-stu-id="98d32-308">View the timing of requests in relation to one another</span></span>   

<span data-ttu-id="98d32-309">Используйте Каскад, чтобы просмотреть время связи между запросами друг с другом.</span><span class="sxs-lookup"><span data-stu-id="98d32-309">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="98d32-310">По умолчанию каскадом упорядочиваются по времени начала запросов.</span><span class="sxs-lookup"><span data-stu-id="98d32-310">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="98d32-311">Таким образом, запросы, которые раньше приступили к началу, чем те, которые находятся дальше по правому краю.</span><span class="sxs-lookup"><span data-stu-id="98d32-311">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="98d32-312">Чтобы увидеть различные способы сортировки каскадов, просмотрите [фазу сортировки по действию](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="98d32-312">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

> ##### <span data-ttu-id="98d32-313">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="98d32-313">Figure 18</span></span>  
> <span data-ttu-id="98d32-314">Столбец "Каскад" на панели "запросы"</span><span class="sxs-lookup"><span data-stu-id="98d32-314">The Waterfall column of the Requests pane</span></span>  
> <span data-ttu-id="98d32-315">! [Столбец каскадов в области запросов] [ImageRequestsTableWaterfallColumn]</span><span class="sxs-lookup"><span data-stu-id="98d32-315">![The Waterfall column of the Requests pane][ImageRequestsTableWaterfallColumn]</span></span>  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
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

### <span data-ttu-id="98d32-316">Предварительный просмотр тела ответа</span><span class="sxs-lookup"><span data-stu-id="98d32-316">View a preview of a response body</span></span>   

<span data-ttu-id="98d32-317">Чтобы предварительно просмотреть текст ответа, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-317">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="98d32-318">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="98d32-318">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98d32-319">Откройте вкладку **Предварительный просмотр** .</span><span class="sxs-lookup"><span data-stu-id="98d32-319">Select the **Preview** tab.</span></span>  

<span data-ttu-id="98d32-320">Эта вкладка особенно полезна для просмотра изображений.</span><span class="sxs-lookup"><span data-stu-id="98d32-320">This tab is mostly useful for viewing images.</span></span>  

> ##### <span data-ttu-id="98d32-321">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="98d32-321">Figure 19</span></span>  
> <span data-ttu-id="98d32-322">Вкладка "предварительный просмотр"</span><span class="sxs-lookup"><span data-stu-id="98d32-322">The Preview tab</span></span>  
> <span data-ttu-id="98d32-323">! [Вкладка "предварительный просмотр"] [ImagePreview]</span><span class="sxs-lookup"><span data-stu-id="98d32-323">![The Preview tab][ImagePreview]</span></span>  

### <span data-ttu-id="98d32-324">Просмотр текста ответа</span><span class="sxs-lookup"><span data-stu-id="98d32-324">View a response body</span></span>   

<span data-ttu-id="98d32-325">Чтобы просмотреть текст ответа на запрос, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-325">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="98d32-326">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="98d32-326">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98d32-327">Откройте вкладку **ответ** .</span><span class="sxs-lookup"><span data-stu-id="98d32-327">Select the **Response** tab.</span></span>  

> ##### <span data-ttu-id="98d32-328">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="98d32-328">Figure 20</span></span>  
> <span data-ttu-id="98d32-329">Вкладка "ответ"</span><span class="sxs-lookup"><span data-stu-id="98d32-329">The Response tab</span></span>  
> <span data-ttu-id="98d32-330">! [Вкладка "ответ"] [ImageResponse]</span><span class="sxs-lookup"><span data-stu-id="98d32-330">![The Response tab][ImageResponse]</span></span>  

### <span data-ttu-id="98d32-331">Просмотр заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="98d32-331">View HTTP headers</span></span>   

<span data-ttu-id="98d32-332">Чтобы просмотреть данные заголовка HTTP для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-332">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="98d32-333">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="98d32-333">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98d32-334">Откройте вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="98d32-334">Select the **Headers** tab.</span></span>  

> ##### <span data-ttu-id="98d32-335">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="98d32-335">Figure 21</span></span>  
> <span data-ttu-id="98d32-336">Вкладка "заголовки"</span><span class="sxs-lookup"><span data-stu-id="98d32-336">The Headers tab</span></span>  
> <span data-ttu-id="98d32-337">! [Вкладка Заголовки] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="98d32-337">![The Headers tab][ImageHeaders]</span></span>  

#### <span data-ttu-id="98d32-338">Просмотр источника заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="98d32-338">View HTTP header source</span></span>   

<span data-ttu-id="98d32-339">По умолчанию на вкладке заголовки отображаются имена заголовков в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="98d32-339">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="98d32-340">Чтобы просмотреть имена HTTP-заголовков в том порядке, в котором они были получены:</span><span class="sxs-lookup"><span data-stu-id="98d32-340">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="98d32-341">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="98d32-341">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="98d32-342">См.: [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="98d32-342">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="98d32-343">Нажмите кнопку **источник**, рядом с разделом **заголовок запроса** или **заголовок ответа** .</span><span class="sxs-lookup"><span data-stu-id="98d32-343">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="98d32-344">Просмотр параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="98d32-344">View query string parameters</span></span>   

<span data-ttu-id="98d32-345">Чтобы просмотреть параметры строки запроса URL-адреса в удобочитаемом формате, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-345">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="98d32-346">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="98d32-346">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="98d32-347">См.: [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="98d32-347">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="98d32-348">Перейдите к разделу **Параметры строки запроса** .</span><span class="sxs-lookup"><span data-stu-id="98d32-348">Go to the **Query String Parameters** section.</span></span>  

> ##### <span data-ttu-id="98d32-349">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="98d32-349">Figure 22</span></span>  
> <span data-ttu-id="98d32-350">Раздел "параметры строки запроса"</span><span class="sxs-lookup"><span data-stu-id="98d32-350">The Query String Parameters section</span></span>  
> <span data-ttu-id="98d32-351">! [Раздел параметров строки запроса] [ImageQueryStringParameters]</span><span class="sxs-lookup"><span data-stu-id="98d32-351">![The Query String Parameters section][ImageQueryStringParameters]</span></span>  

#### <span data-ttu-id="98d32-352">Просмотр источника параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="98d32-352">View query string parameters source</span></span>   

<span data-ttu-id="98d32-353">Чтобы просмотреть источник параметра строки запроса для запроса:</span><span class="sxs-lookup"><span data-stu-id="98d32-353">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="98d32-354">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="98d32-354">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="98d32-355">Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="98d32-355">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="98d32-356">Нажмите кнопку **Просмотр источника**.</span><span class="sxs-lookup"><span data-stu-id="98d32-356">Select **view source**.</span></span>  

#### <span data-ttu-id="98d32-357">Просмотр строковых параметров запроса в кодировке URL</span><span class="sxs-lookup"><span data-stu-id="98d32-357">View URL-encoded query string parameters</span></span>   

<span data-ttu-id="98d32-358">Чтобы просмотреть параметры строки запроса в удобочитаемом формате, но с сохранением кодировки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-358">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="98d32-359">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="98d32-359">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="98d32-360">Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="98d32-360">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="98d32-361">Выберите команду **Просмотреть закодированный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="98d32-361">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="98d32-362">Просмотр файлов cookie</span><span class="sxs-lookup"><span data-stu-id="98d32-362">View cookies</span></span>   

<span data-ttu-id="98d32-363">Чтобы просмотреть cookie-файлы, отправленные в заголовке HTTP запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-363">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="98d32-364">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="98d32-364">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98d32-365">Перейдите на вкладку " **cookie** ".</span><span class="sxs-lookup"><span data-stu-id="98d32-365">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

> ##### <span data-ttu-id="98d32-366">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="98d32-366">Figure 23</span></span>  
> <span data-ttu-id="98d32-367">Вкладка "cookie"</span><span class="sxs-lookup"><span data-stu-id="98d32-367">The Cookies tab</span></span>  
> <span data-ttu-id="98d32-368">! [Вкладка "cookie"] [ImageCookies]</span><span class="sxs-lookup"><span data-stu-id="98d32-368">![The Cookies tab][ImageCookies]</span></span>  

### <span data-ttu-id="98d32-369">Просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="98d32-369">View the timing breakdown of a request</span></span>   

<span data-ttu-id="98d32-370">Чтобы просмотреть межвременную разбивку запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-370">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="98d32-371">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="98d32-371">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98d32-372">Откройте вкладку **время** .</span><span class="sxs-lookup"><span data-stu-id="98d32-372">Select the **Timing** tab.</span></span>  

<span data-ttu-id="98d32-373">Дополнительные сведения можно найти в разделе [Предварительный просмотр разбивки времени](#preview-a-timing-breakdown) для доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="98d32-373">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="98d32-374">Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке время, приведены в разделе [этапы разбиения по времени](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="98d32-374">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

> ##### <span data-ttu-id="98d32-375">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="98d32-375">Figure 24</span></span>  
> <span data-ttu-id="98d32-376">Вкладка время</span><span class="sxs-lookup"><span data-stu-id="98d32-376">The Timing tab</span></span>  
> <span data-ttu-id="98d32-377">! [Вкладка время] [ImageTiming]</span><span class="sxs-lookup"><span data-stu-id="98d32-377">![The Timing tab][ImageTiming]</span></span>  

<span data-ttu-id="98d32-378">Дополнительные сведения о каждой из фаз.</span><span class="sxs-lookup"><span data-stu-id="98d32-378">More information about each of the phases.</span></span>  

<span data-ttu-id="98d32-379">Другие способы доступа к этому представлению можно найти в разделе [Просмотр временных интервалов](#view-the-timing-breakdown-of-a-request) .</span><span class="sxs-lookup"><span data-stu-id="98d32-379">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="98d32-380">Предварительный просмотр разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="98d32-380">Preview a timing breakdown</span></span>   

<span data-ttu-id="98d32-381">Чтобы просмотреть сведения о разбиении по времени для запроса, наведите указатель мыши на запись запроса в столбце **Каскад** таблицы запросы.</span><span class="sxs-lookup"><span data-stu-id="98d32-381">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="98d32-382">Ознакомьтесь [со](#view-the-timing-breakdown-of-a-request) сведениями о том, как получить доступ к данным, которые не требуют наведения мыши, в запросе.</span><span class="sxs-lookup"><span data-stu-id="98d32-382">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

> ##### <span data-ttu-id="98d32-383">Рис. 25</span><span class="sxs-lookup"><span data-stu-id="98d32-383">Figure 25</span></span>  
> <span data-ttu-id="98d32-384">Предварительный просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="98d32-384">Previewing the timing breakdown of a request</span></span>  
> <span data-ttu-id="98d32-385">! [Предварительный просмотр разбиения по времени для запроса] [ImageWaterfallHover]</span><span class="sxs-lookup"><span data-stu-id="98d32-385">![Previewing the timing breakdown of a request][ImageWaterfallHover]</span></span>  

#### <span data-ttu-id="98d32-386">Описание этапов разделения времени</span><span class="sxs-lookup"><span data-stu-id="98d32-386">Timing breakdown phases explained</span></span>   

<span data-ttu-id="98d32-387">Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке время:</span><span class="sxs-lookup"><span data-stu-id="98d32-387">More information about each of the phases you may see in the Timing tab:</span></span>  

*   <span data-ttu-id="98d32-388">**Очереди**.</span><span class="sxs-lookup"><span data-stu-id="98d32-388">**Queueing**.</span></span>  <span data-ttu-id="98d32-389">Браузер помещает запросы в очередь в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="98d32-389">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="98d32-390">Существуют запросы с более высокими приоритетами.</span><span class="sxs-lookup"><span data-stu-id="98d32-390">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="98d32-391">Для этого происхождения уже открыто шесть подключений TCP, что является ограничением.</span><span class="sxs-lookup"><span data-stu-id="98d32-391">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="98d32-392">Применимо только к HTTP/1.0 и HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="98d32-392">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="98d32-393">Браузер временно выделяет место в кэше на диске.</span><span class="sxs-lookup"><span data-stu-id="98d32-393">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="98d32-394">**Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="98d32-394">**Stalled**.</span></span>  <span data-ttu-id="98d32-395">Запрос может быть остановлен в любой из причин, описанных в разделе **очереди**.</span><span class="sxs-lookup"><span data-stu-id="98d32-395">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="98d32-396">**Поиск DNS**.</span><span class="sxs-lookup"><span data-stu-id="98d32-396">**DNS Lookup**.</span></span>  <span data-ttu-id="98d32-397">Браузер разрешает IP-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="98d32-397">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="98d32-398">**Согласование прокси-сервера**.</span><span class="sxs-lookup"><span data-stu-id="98d32-398">**Proxy negotiation**.</span></span>  <span data-ttu-id="98d32-399">Браузер согласовывает запрос с [прокси-сервером][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="98d32-399">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="98d32-400">**Запрос отправлен**.</span><span class="sxs-lookup"><span data-stu-id="98d32-400">**Request sent**.</span></span>  <span data-ttu-id="98d32-401">Запрос отправляется.</span><span class="sxs-lookup"><span data-stu-id="98d32-401">The request is being sent.</span></span>  
*   <span data-ttu-id="98d32-402">**Подготовка ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="98d32-402">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="98d32-403">Браузер запускает сервисный рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="98d32-403">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="98d32-404">**Запросите ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="98d32-404">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="98d32-405">Запрос отправляется сотруднику службы.</span><span class="sxs-lookup"><span data-stu-id="98d32-405">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="98d32-406">**Ожидание \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="98d32-406">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="98d32-407">Браузер ожидает первый байт ответа.</span><span class="sxs-lookup"><span data-stu-id="98d32-407">The browser is waiting for the first byte of a response.</span></span>  
  <span data-ttu-id="98d32-408">TTFB означает время для первого байта.</span><span class="sxs-lookup"><span data-stu-id="98d32-408">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="98d32-409">Это время включает 1 круговый путь задержки и время, затраченное сервером на подготовку ответа.</span><span class="sxs-lookup"><span data-stu-id="98d32-409">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="98d32-410">**Загрузка содержимого**.</span><span class="sxs-lookup"><span data-stu-id="98d32-410">**Content Download**.</span></span>  <span data-ttu-id="98d32-411">Браузер получает ответ.</span><span class="sxs-lookup"><span data-stu-id="98d32-411">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="98d32-412">**Получение push-уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="98d32-412">**Receiving Push**.</span></span>  <span data-ttu-id="98d32-413">Браузер получает данные для этого ответа через HTTP/2 серверную извещающую передачу.</span><span class="sxs-lookup"><span data-stu-id="98d32-413">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="98d32-414">**Чтение push-уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="98d32-414">**Reading Push**.</span></span>  <span data-ttu-id="98d32-415">Браузер читает локальные данные, полученные ранее.</span><span class="sxs-lookup"><span data-stu-id="98d32-415">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="98d32-416">Просмотр инициаторов и зависимостей</span><span class="sxs-lookup"><span data-stu-id="98d32-416">View initiators and dependencies</span></span>   

<span data-ttu-id="98d32-417">Чтобы просмотреть инициаторы и зависимости запроса, удерживайте `Shift` и наведите указатель мыши на запрос в таблице запросы.</span><span class="sxs-lookup"><span data-stu-id="98d32-417">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="98d32-418">DevTools цвета: инициаторы отображаются зеленым цветом, а зависимости — красным.</span><span class="sxs-lookup"><span data-stu-id="98d32-418">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

> ##### <span data-ttu-id="98d32-419">Рис. 26</span><span class="sxs-lookup"><span data-stu-id="98d32-419">Figure 26</span></span>  
> <span data-ttu-id="98d32-420">Просмотр инициаторов и зависимостей запроса</span><span class="sxs-lookup"><span data-stu-id="98d32-420">Viewing the initiators and dependencies of a request</span></span>  
> <span data-ttu-id="98d32-421">! [Просмотр инициаторов и зависимостей запроса] [ImageRequestInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="98d32-421">![Viewing the initiators and dependencies of a request][ImageRequestInitiatorsDependencies]</span></span>  

<span data-ttu-id="98d32-422">Когда таблица запросов упорядочивается в хронологическом порядке, первым зеленым запросом над ним, который вы наводите, является инициатор зависимости.</span><span class="sxs-lookup"><span data-stu-id="98d32-422">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="98d32-423">Если над ним появится еще один зеленый запрос, этот более высокий запрос является инициатором инициатора.</span><span class="sxs-lookup"><span data-stu-id="98d32-423">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="98d32-424">И так далее.</span><span class="sxs-lookup"><span data-stu-id="98d32-424">And so on.</span></span>  

### <span data-ttu-id="98d32-425">Просмотр событий загрузки</span><span class="sxs-lookup"><span data-stu-id="98d32-425">View load events</span></span>   

<span data-ttu-id="98d32-426">DevTools отображает время показа `DOMContentLoaded` `load` событий в нескольких местах на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="98d32-426">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="98d32-427">`DOMContentLoaded`Событие окрашивается синим цветом, а `load` событие — красным.</span><span class="sxs-lookup"><span data-stu-id="98d32-427">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

> ##### <span data-ttu-id="98d32-428">На рисунке 27</span><span class="sxs-lookup"><span data-stu-id="98d32-428">Figure 27</span></span>  
> <span data-ttu-id="98d32-429">Расположение `DOMContentLoaded` событий "и" `load` на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="98d32-429">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
> <span data-ttu-id="98d32-430">! [Расположение событий DOMContentLoaded и Load на панели "сеть"] [ImageNetworkPanelDOMContentLoadedLoadEvents]</span><span class="sxs-lookup"><span data-stu-id="98d32-430">![The locations of the DOMContentLoaded and load events on the Network panel][ImageNetworkPanelDOMContentLoadedLoadEvents]</span></span>  

### <span data-ttu-id="98d32-431">Просмотр общего числа запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-431">View the total number of requests</span></span>   

<span data-ttu-id="98d32-432">Общее количество запросов можно найти в области сводки в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="98d32-432">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="98d32-433">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="98d32-433">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="98d32-434">Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="98d32-434">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="98d32-435">Рис. 28</span><span class="sxs-lookup"><span data-stu-id="98d32-435">Figure 28</span></span>  
> <span data-ttu-id="98d32-436">Общее количество запросов с момента открытия DevTools</span><span class="sxs-lookup"><span data-stu-id="98d32-436">The total number of requests since DevTools was opened</span></span>  
> <span data-ttu-id="98d32-437">! [Общее количество запросов с момента открытия DevTools] [ImageTotalRequests]</span><span class="sxs-lookup"><span data-stu-id="98d32-437">![The total number of requests since DevTools was opened][ImageTotalRequests]</span></span>  

### <span data-ttu-id="98d32-438">Просмотр общего объема загружаемого файла</span><span class="sxs-lookup"><span data-stu-id="98d32-438">View the total download size</span></span>   

<span data-ttu-id="98d32-439">Общий объем загруженных запросов отображается в области Сводка в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="98d32-439">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="98d32-440">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="98d32-440">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="98d32-441">Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="98d32-441">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="98d32-442">Рис. 29</span><span class="sxs-lookup"><span data-stu-id="98d32-442">Figure 29</span></span>  
> <span data-ttu-id="98d32-443">Общий объем загруженных запросов</span><span class="sxs-lookup"><span data-stu-id="98d32-443">The total download size of requests</span></span>  
> <span data-ttu-id="98d32-444">! [Общий размер загружаемых запросов] [ImageTotalSize]</span><span class="sxs-lookup"><span data-stu-id="98d32-444">![The total download size of requests][ImageTotalSize]</span></span>  

<span data-ttu-id="98d32-445">[Просмотр несжатого размера ресурса](#view-the-uncompressed-size-of-a-resource) для просмотра больших ресурсов после того, как браузер распаковывает каждый элемент.</span><span class="sxs-lookup"><span data-stu-id="98d32-445">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="98d32-446">Просмотр трассировки стека, которая привела к запросу</span><span class="sxs-lookup"><span data-stu-id="98d32-446">View the stack trace that caused a request</span></span>   

<span data-ttu-id="98d32-447">После того, как инструкция JavaScript запрашивает ресурс, наведите указатель мыши на столбец **инициатора** , чтобы просмотреть трассировку стека, выступающей в запрос.</span><span class="sxs-lookup"><span data-stu-id="98d32-447">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

> ##### <span data-ttu-id="98d32-448">Рис. 30</span><span class="sxs-lookup"><span data-stu-id="98d32-448">Figure 30</span></span>  
> <span data-ttu-id="98d32-449">Трассировка стека, ведущая к запросу ресурсов</span><span class="sxs-lookup"><span data-stu-id="98d32-449">The stack trace leading up to a resource request</span></span>  
> <span data-ttu-id="98d32-450">! [Трассировка стека, ведущая к запросу ресурсов] [ImageInitiatorStack]</span><span class="sxs-lookup"><span data-stu-id="98d32-450">![The stack trace leading up to a resource request][ImageInitiatorStack]</span></span>  

### <span data-ttu-id="98d32-451">Просмотр несжатого размера ресурса</span><span class="sxs-lookup"><span data-stu-id="98d32-451">View the uncompressed size of a resource</span></span>   

<span data-ttu-id="98d32-452">Установите флажок **использовать строки большого запроса** , а затем посмотрите на нижнее значение столбца **Размер** .</span><span class="sxs-lookup"><span data-stu-id="98d32-452">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

> ##### <span data-ttu-id="98d32-453">На рисунке 31</span><span class="sxs-lookup"><span data-stu-id="98d32-453">Figure 31</span></span>  
> <span data-ttu-id="98d32-454">Пример несжатых ресурсов \ (сжатый размер `jquery-3.3.1.min.js` файла, отправленного по сети `29.9 KB` , в то время как несжатый размер `84.9 KB` )</span><span class="sxs-lookup"><span data-stu-id="98d32-454">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
> <span data-ttu-id="98d32-455">! [Пример несжатых ресурсов] [ImageUncompressedResources]</span><span class="sxs-lookup"><span data-stu-id="98d32-455">![An example of uncompressed resources][ImageUncompressedResources]</span></span>  

## <span data-ttu-id="98d32-456">Данные запросов на экспорт</span><span class="sxs-lookup"><span data-stu-id="98d32-456">Export requests data</span></span>   

### <span data-ttu-id="98d32-457">Сохранение всех сетевых запросов в файле HAR</span><span class="sxs-lookup"><span data-stu-id="98d32-457">Save all network requests to a HAR file</span></span>   

<span data-ttu-id="98d32-458">Чтобы сохранить все сетевые запросы в файле HAR, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="98d32-458">To save all network requests to a HAR file:</span></span>  

1.  <span data-ttu-id="98d32-459">Щелкните правой кнопкой мыши любой запрос в таблице "запросы".</span><span class="sxs-lookup"><span data-stu-id="98d32-459">Right-click any request in the Requests table.</span></span>  
1.  <span data-ttu-id="98d32-460">Выберите команду **Сохранить как HAR с содержимым**.</span><span class="sxs-lookup"><span data-stu-id="98d32-460">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="98d32-461">DevTools сохраняет все запросы, произошедшие после того, как вы открыли DevTools в файл HAR.</span><span class="sxs-lookup"><span data-stu-id="98d32-461">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="98d32-462">Невозможно отфильтровать запросы или сохранить только один запрос.</span><span class="sxs-lookup"><span data-stu-id="98d32-462">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="98d32-463">После того как вы сохраните файл HAR, вы можете импортировать его обратно в DevTools для анализа.</span><span class="sxs-lookup"><span data-stu-id="98d32-463">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="98d32-464">Просто перетащите файл HAR в таблицу запросы.</span><span class="sxs-lookup"><span data-stu-id="98d32-464">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### <span data-ttu-id="98d32-465">Рисунок 32</span><span class="sxs-lookup"><span data-stu-id="98d32-465">Figure 32</span></span>  
> <span data-ttu-id="98d32-466">Выбор команды "Сохранить как HAR с контентом"</span><span class="sxs-lookup"><span data-stu-id="98d32-466">Selecting Save as HAR with Content</span></span>  
> <span data-ttu-id="98d32-467">! [Выберите команду Сохранить как HAR с содержимым] [ImageSaveAsHAR]</span><span class="sxs-lookup"><span data-stu-id="98d32-467">![Selecting Save as HAR with Content][ImageSaveAsHAR]</span></span>  

### <span data-ttu-id="98d32-468">Копирование одного или нескольких запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="98d32-468">Copy one or more requests to the clipboard</span></span>   

<span data-ttu-id="98d32-469">В столбце **имя** таблицы запросы щелкните запрос правой кнопкой мыши, наведите указатель на пункт **Копировать**и выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="98d32-469">Under the **Name** column of the Requests table, right-click a request, hover over **Copy**, and select one of the following options:</span></span>  

*   <span data-ttu-id="98d32-470">**Копировать адрес ссылки**.</span><span class="sxs-lookup"><span data-stu-id="98d32-470">**Copy Link Address**.</span></span>  <span data-ttu-id="98d32-471">Скопируйте URL-адрес запроса в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="98d32-471">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="98d32-472">**Копирование ответа**.</span><span class="sxs-lookup"><span data-stu-id="98d32-472">**Copy Response**.</span></span>  <span data-ttu-id="98d32-473">Скопировать текст ответа в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="98d32-473">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="98d32-474">**Копировать как выборку**.</span><span class="sxs-lookup"><span data-stu-id="98d32-474">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="98d32-475">**Копировать как фигуру**.</span><span class="sxs-lookup"><span data-stu-id="98d32-475">**Copy as cURL**.</span></span>  <span data-ttu-id="98d32-476">Копирование запроса в виде текстовой команды.</span><span class="sxs-lookup"><span data-stu-id="98d32-476">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="98d32-477">**Копировать все как выборку**.</span><span class="sxs-lookup"><span data-stu-id="98d32-477">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="98d32-478">**Скопировать все как фигуру**.</span><span class="sxs-lookup"><span data-stu-id="98d32-478">**Copy All as cURL**.</span></span>  <span data-ttu-id="98d32-479">Копирование всех запросов в виде последовательности команд с фигурой.</span><span class="sxs-lookup"><span data-stu-id="98d32-479">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="98d32-480">**Копировать все как HAR**.</span><span class="sxs-lookup"><span data-stu-id="98d32-480">**Copy All as HAR**.</span></span>  <span data-ttu-id="98d32-481">Скопируйте все запросы как данные HAR.</span><span class="sxs-lookup"><span data-stu-id="98d32-481">Copy all requests as HAR data.</span></span>  

> ##### <span data-ttu-id="98d32-482">Рисунок 33</span><span class="sxs-lookup"><span data-stu-id="98d32-482">Figure 33</span></span>  
> <span data-ttu-id="98d32-483">Выбор пункта "Копировать ответ"</span><span class="sxs-lookup"><span data-stu-id="98d32-483">Selecting Copy Response</span></span>  
> <span data-ttu-id="98d32-484">! [Выберите команду ' ' Копировать ответ] ' ' [ImageCopyResponse]</span><span class="sxs-lookup"><span data-stu-id="98d32-484">![Selecting Copy Response][ImageCopyResponse]</span></span>  

## <span data-ttu-id="98d32-485">Изменение макета панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="98d32-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="98d32-486">Вы можете развернуть или свернуть разделы пользовательского интерфейса панели "сеть", чтобы сосредоточиться на важных сведениях.</span><span class="sxs-lookup"><span data-stu-id="98d32-486">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="98d32-487">Скрытие области фильтров</span><span class="sxs-lookup"><span data-stu-id="98d32-487">Hide the Filters pane</span></span>   

<span data-ttu-id="98d32-488">По умолчанию в DevTools отображается **область фильтров**.</span><span class="sxs-lookup"><span data-stu-id="98d32-488">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="98d32-489">Щелкните фильтр **фильтра** ![ ][ImageFilterIcon] , чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="98d32-489">Select **Filter** ![Filter][ImageFilterIcon]  to hide it.</span></span>  

> ##### <span data-ttu-id="98d32-490">Рисунок 34</span><span class="sxs-lookup"><span data-stu-id="98d32-490">Figure 34</span></span>  
> <span data-ttu-id="98d32-491">Кнопка "скрыть фильтры"</span><span class="sxs-lookup"><span data-stu-id="98d32-491">The Hide Filters button</span></span>  
> <span data-ttu-id="98d32-492">! [Кнопка "скрыть фильтры"] [ImageHideFiltersButton]</span><span class="sxs-lookup"><span data-stu-id="98d32-492">![The Hide Filters button][ImageHideFiltersButton]</span></span>  

### <span data-ttu-id="98d32-493">Использование строк большого запроса</span><span class="sxs-lookup"><span data-stu-id="98d32-493">Use large request rows</span></span>   

<span data-ttu-id="98d32-494">Используйте большие строки, если вы хотите, чтобы в таблице сетевых запросов больше пробелов.</span><span class="sxs-lookup"><span data-stu-id="98d32-494">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="98d32-495">Некоторые столбцы также содержат дополнительные сведения при использовании больших строк.</span><span class="sxs-lookup"><span data-stu-id="98d32-495">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="98d32-496">Например, минимальное значение столбца « **Размер** » — это несжатый размер запроса.</span><span class="sxs-lookup"><span data-stu-id="98d32-496">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

> ##### <span data-ttu-id="98d32-497">Рисунок 35</span><span class="sxs-lookup"><span data-stu-id="98d32-497">Figure 35</span></span>  
> <span data-ttu-id="98d32-498">Пример строк большого запроса в области "запросы"</span><span class="sxs-lookup"><span data-stu-id="98d32-498">An example of large request rows in the Requests pane</span></span>  
> <span data-ttu-id="98d32-499">! [Пример строк большого запроса в области запросов] [ImageLargeRequestRows]</span><span class="sxs-lookup"><span data-stu-id="98d32-499">![An example of large request rows in the Requests pane][ImageLargeRequestRows]</span></span>  

<span data-ttu-id="98d32-500">Установите флажок **использовать строки большого запроса** , чтобы включить большие строки.</span><span class="sxs-lookup"><span data-stu-id="98d32-500">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

> ##### <span data-ttu-id="98d32-501">Рисунок 36</span><span class="sxs-lookup"><span data-stu-id="98d32-501">Figure 36</span></span>  
> <span data-ttu-id="98d32-502">Флажок "строки большого запроса"</span><span class="sxs-lookup"><span data-stu-id="98d32-502">The Large Request Rows checkbox</span></span>  
> <span data-ttu-id="98d32-503">! [Флажок "строки большого запроса"] [ImageLargeRequestRowsCheckbox]</span><span class="sxs-lookup"><span data-stu-id="98d32-503">![The Large Request Rows checkbox][ImageLargeRequestRowsCheckbox]</span></span>  

### <span data-ttu-id="98d32-504">Скрытие области обзора</span><span class="sxs-lookup"><span data-stu-id="98d32-504">Hide the Overview pane</span></span>   

<span data-ttu-id="98d32-505">По умолчанию в DevTools отображается **область "Общие сведения**".</span><span class="sxs-lookup"><span data-stu-id="98d32-505">By default, DevTools shows the **Overview pane**.</span></span>  
<span data-ttu-id="98d32-506">Снимите флажок **Показать общие сведения** , чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="98d32-506">Deselect the **Show Overview** checkbox to hide it.</span></span>  

> ##### <span data-ttu-id="98d32-507">Рисунок 37</span><span class="sxs-lookup"><span data-stu-id="98d32-507">Figure 37</span></span>  
> <span data-ttu-id="98d32-508">Флажок "Показать общие сведения"</span><span class="sxs-lookup"><span data-stu-id="98d32-508">The Show Overview checkbox</span></span>  
> <span data-ttu-id="98d32-509">! [Флажок Показать общие сведения] [ImageHideOverviewCheckbox]</span><span class="sxs-lookup"><span data-stu-id="98d32-509">![The Show Overview checkbox][ImageHideOverviewCheckbox]</span></span>  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Рисунок 1: панель "сеть""  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Рисунок 2: кнопка "очистить""  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Рисунок 3: флажок "сохранить журнал""  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Рисунок 4: наведение указателя на снимок экрана"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Disable-Cache-CheckBox.MSFT.png "Рисунок 5: флажок отключения кэша"  
[ImageClearBrowserCache]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-Cache.MSFT.png "Рисунок 6: выбор команды очистки кэша браузера"  
[ImageOfflineDropdown]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-offline-DropDown.MSFT.png "Рисунок 7: раскрывающийся список" в автономном режиме "  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Throttling-Menu.MSFT.png "Рисунок 8: меню регулирования сети"  
[ImageClearBrowserCookies]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-cookies.MSFT.png "Рисунок 9: выбор пункта" очистить "cookie-файлы браузера"  
[ImageFilterTextBox]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Filters-TextBox.MSFT.png "Рисунок 10: текстовое поле" фильтры "  
[ImageMultiTypeFilter]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Type-Filters.MSFT.png "Рисунок 11: использование фильтров типов для отображения ресурсов JS, CSS и документов"  
[ImageOverviewFilter]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Overview-Filter.MSFT.png "Рисунок 12: фильтрация всех неактивных запросов, которые были неактивны вокруг 300ms"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Hide-Data-URLs.MSFT.png "Рисунок 13: флажок" скрыть URL-адреса данных "  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Waterfall-Total-Duration.MSFT.png "Рисунок 14: Сортировка каскадом по общей длительности"  
[ImageRequestsTable]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Table.MSFT.png "Рисунок 15: таблица запросов"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Add-Column.MSFT.png "Рисунок 16: Добавление столбца в таблицу" запросы "  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Add-Custom.MSFT.png "Рисунок 17: Добавление настраиваемого столбца в таблицу" запросы "  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Waterfall.MSFT.png "Рисунок 18: столбец каскадом на панели" запросы "  
[ImagePreview]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-Preview.MSFT.png "Рисунок 19: вкладка" предварительный просмотр "  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[ImageResponse]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-Response.MSFT.png "Рисунок 20: вкладка" ответ ""  
[ImageHeaders]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Resources-Headers.MSFT.png "Рисунок 21: вкладка" заголовки "  
[ImageQueryStringParameters]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-Headers-Query-String-Parameters.MSFT.png "рис. 22: раздел" параметры строки запроса "  
[ImageCookies]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-cookies.MSFT.png "рис 23: вкладка" cookie "  
[ImageTiming]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-Timing.MSFT.png "Рисунок 24: вкладка" время "  
[ImageWaterfallHover]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-Hover.MSFT.png "Рисунок 25: предварительный просмотр разбиения времени запроса"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-Initiators-DEPENDENCIES.MSFT.png "Рисунок 26: Просмотр инициаторов и зависимостей запроса"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Load-Events.MSFT.png "Рисунок 27: расположение событий" DOMContentLoaded "и" Загрузить "на панели" сеть "  
[ImageTotalRequests]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Total-requests.MSFT.png "Рисунок 28: общее количество запросов с момента открытия DevTools"  
[ImageTotalSize]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Total-download-size.MSFT.png "Рисунок 29: общий объем загружаемого запроса"  
[ImageInitiatorStack]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Initiator-Stack.MSFT.png "Рисунок 30: трассировка стека, ведущая к запросу ресурсов"  
[ImageUncompressedResources]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-uncompressed-Compare.MSFT.png "Рисунок 31: пример несжатых ресурсов"  
[ImageSaveAsHAR]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Save-Har-Content.MSFT.png "Рисунок 32: выбор команды" Сохранить как HAR с содержимым "  
[ImageCopyResponse]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Copy-Response.MSFT.png "Рисунок 33: выбор пункта" Копировать ответ "  
[ImageHideFiltersButton]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Resources-Hide-Filters-Button.MSFT.png "Рисунок 34: кнопка" скрыть фильтры "  
[ImageLargeRequestRows]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Large-Request-Rows.MSFT.png "Рисунок 35: пример строк большого запроса в области" запросы "  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-use-Large-Request-Rows-on.MSFT.png "Рисунок 36: флажок" большие строки запросов "  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Network-Requests-Show-Overview-Off.MSFT.png "Рисунок 37: флажок" скрыть общие сведения ""  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Отладка последовательного веб-приложения"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедии"  

> [!NOTE]
> <span data-ttu-id="98d32-550">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="98d32-550">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="98d32-551">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="98d32-551">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="98d32-553">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="98d32-553">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

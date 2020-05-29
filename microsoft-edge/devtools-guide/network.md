---
description: Мониторинг и профилирование запросов ресурсов страниц с помощью панели "сеть"
title: DevTools-Network (сеть)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, сеть, время загрузки, HTTP, HTTPS, кэш браузера, HAR
ms.custom: seodec18
ms.openlocfilehash: 0b190f5163f9b7a9f9920877a94577177053e4f6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571731"
---
# <span data-ttu-id="1ea4e-104">Сеть</span><span class="sxs-lookup"><span data-stu-id="1ea4e-104">Network</span></span>

<span data-ttu-id="1ea4e-105">С помощью панели **Network (сеть** ) можно отслеживать, проверять и профилировать запросы и ответы, отправляемые по каналу связи.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-105">Use the **Network** panel to monitor, inspect and profile the requests and responses sent over the wire.</span></span> <span data-ttu-id="1ea4e-106">С его помощью вы можете:</span><span class="sxs-lookup"><span data-stu-id="1ea4e-106">With it, you can:</span></span>

 - <span data-ttu-id="1ea4e-107">[Просмотр записи всех запросов ресурсов](#network-summary) , сделанных страницей</span><span class="sxs-lookup"><span data-stu-id="1ea4e-107">[Browse a record of all the resource requests](#network-summary) made by the page</span></span>
 - <span data-ttu-id="1ea4e-108">[Измерение времени загрузки сайта](#summary-bar) для нового и возвращающего пользователей</span><span class="sxs-lookup"><span data-stu-id="1ea4e-108">[Measure the load time of your site](#summary-bar) for new and returning users</span></span> 
 - <span data-ttu-id="1ea4e-109">[Проверка заголовков, основных текстов сообщений, параметров и файлов cookie, которые](#request-details) обмениваются между страницей и сетью</span><span class="sxs-lookup"><span data-stu-id="1ea4e-109">[Inspect the headers, message bodies, parameters, and cookies](#request-details) exchanged between your page and the network</span></span>
 - <span data-ttu-id="1ea4e-110">[Определение сетевых событий, вызывающих узкие места](#timings) во время загрузки сайта</span><span class="sxs-lookup"><span data-stu-id="1ea4e-110">[Identify the network events causing bottlenecks](#timings) in the load time of your site</span></span>

![Панель DevTools сети Microsoft Edge](./media/network.png)

## <span data-ttu-id="1ea4e-112">Сводка по сети</span><span class="sxs-lookup"><span data-stu-id="1ea4e-112">Network summary</span></span>

<span data-ttu-id="1ea4e-113">Когда вы открываете DevTools, сетевое Профилирование включается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-113">When you open  DevTools, network profiling is turned on by default.</span></span> <span data-ttu-id="1ea4e-114">Весь сетевой трафик с активной вкладки браузера записывается в списке "Сводка сети" даже в том случае, если вы работаете на другой DevTools панели, чем в *сети*.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-114">All the network traffic from your active browser tab is recorded in the network summary list, even while you are working in a different  DevTools panel than *Network*.</span></span>

![Индикатор выполняющегося профилирования в сети](./media/network_profile_indicator.png)

### <span data-ttu-id="1ea4e-116">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="1ea4e-116">Toolbar</span></span>

<span data-ttu-id="1ea4e-117">На панели инструментов находятся элементы управления для профилирования и фильтрации активности сети на странице.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-117">The toolbar provides controls for profiling and filtering the network activity of your page.</span></span> 

![Панель инструментов "профилировщик сети"](./media/network_toolbar.png)

1. <span data-ttu-id="1ea4e-119">**Запуск и остановка сеанса профилирования**: по умолчанию используется сетевое профилирование, а сетевой трафик заносится в список [**сетевых профайлеров**](#network-request-list) .</span><span class="sxs-lookup"><span data-stu-id="1ea4e-119">**Start / Stop profiling session**: By default, network profiling is turned on, and network traffic will be logged in the [**Network profiler**](#network-request-list) list.</span></span> <span data-ttu-id="1ea4e-120">Вы можете отключить захват сети с помощью кнопки **Stop** "остановить `Ctrl+E` " ().</span><span class="sxs-lookup"><span data-stu-id="1ea4e-120">You can turn off network capture with the **Stop** (`Ctrl+E`) button.</span></span>

2. <span data-ttu-id="1ea4e-121">**Экспортировать как HAR**: вы можете сохранить текущий сеанс профилирования в сети ( `Ctrl+S` ) в виде файла [архива НТТР (HAR)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-121">**Export as HAR**: You can save the current network profiling session (`Ctrl+S`) as a JSON-formatted [HTTP Archive (HAR)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) file.</span></span> 

3. <span data-ttu-id="1ea4e-122">**Фильтр по типу контента**: отфильтровать список сетевых запросов по конкретным запросам содержимого (*документы, таблицы стилей, изображения, сценарии, мультимедиа, шрифты, XHR, другие*).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-122">**Content type filter**: Filter the network request list by specific content requests (*Documents, Style sheets, Images, Scripts, Media, Fonts, XHR, Other*).</span></span> <span data-ttu-id="1ea4e-123">По умолчанию отображаются все типы контента.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-123">By default all content types are shown.</span></span>

4. <span data-ttu-id="1ea4e-124">**Find**: Filter ( `Ctrl+F` ) список сетевых запросов с именами записей (путями ресурсов), содержащими указанную строку поиска.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-124">**Find**: Filter (`Ctrl+F`) the network request list by entry names (resource paths) containing a specified search string.</span></span>

5. <span data-ttu-id="1ea4e-125">**Всегда обновлять с сервера**: нажатие этой кнопки приведет к принудительной загрузке ресурсов страницы из сети, а не кэша браузера.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-125">**Always refresh from server**: Depressing this button will force page resources to load from the network rather than the browser cache.</span></span> <span data-ttu-id="1ea4e-126">Вы можете обновить страницу по сети в один раз, нажав `Ctrl+F5` .</span><span class="sxs-lookup"><span data-stu-id="1ea4e-126">You can refresh the page from  network a single time by pressing `Ctrl+F5`.</span></span>

6. <span data-ttu-id="1ea4e-127">**Обход рабочего процесса для всех сетевых запросов**: отключение зарегистрированных сотрудников службы в качестве сетевых прокси.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-127">**Bypass Service Worker for all network requests**: Disable your registered service workers as network proxies.</span></span> 

7. <span data-ttu-id="1ea4e-128">Кнопки "очистить"</span><span class="sxs-lookup"><span data-stu-id="1ea4e-128">Clear buttons</span></span>

   - <span data-ttu-id="1ea4e-129">**Очистить кэш**: удаляет все ресурсы, хранящиеся в кэше браузера (и эмулирует первый процесс загрузки страницы).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-129">**Clear cache**: Removes all resources stored in the browser cache (and emulates a first-time experience loading the page).</span></span>
   - <span data-ttu-id="1ea4e-130">**Очистка файлов cookie**: удаляет все cookie-файлы для данного домена (и эмулирует процесс первого запуска сайта).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-130">**Clear cookies**: Removes all cookies for the given domain (and emulates a first-time experience of the site).</span></span>
   - <span data-ttu-id="1ea4e-131">**Очистить записи на**навигации: записанный трафик очищается при навигации по страницам.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-131">**Clear entries on navigate**: Recorded traffic is cleared upon page navigation.</span></span> <span data-ttu-id="1ea4e-132">Этот режим включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-132">This is turned on by default.</span></span>
   - <span data-ttu-id="1ea4e-133">**Очистка сеанса**: удаляет все записи сетевого запроса из сводного списка **сети** .</span><span class="sxs-lookup"><span data-stu-id="1ea4e-133">**Clear session**: Clears all network request entries from the **Network summary** list.</span></span>

### <span data-ttu-id="1ea4e-134">Список сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="1ea4e-134">Network request list</span></span>

<span data-ttu-id="1ea4e-135">Весь сетевой трафик записывается в список (до тех пор, пока они не будут очищены при навигации, не будут удалены вручную или DevTools закрываются).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-135">All network traffic is recorded to a list (until cleared upon navigation, manually cleared, or  DevTools are closed).</span></span> <span data-ttu-id="1ea4e-136">Если щелкнуть любую запись, откроется более [подробное представление запроса](#request-details).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-136">Clicking on any entry will open a more [detailed view of the request](#request-details).</span></span>

![Список сетевых запросов](./media/network_request_list.png)

<span data-ttu-id="1ea4e-138">Список сетевых запросов содержит следующие данные:</span><span class="sxs-lookup"><span data-stu-id="1ea4e-138">The network request list includes the following info:</span></span> 

<span data-ttu-id="1ea4e-139">Столбец</span><span class="sxs-lookup"><span data-stu-id="1ea4e-139">Column</span></span> | <span data-ttu-id="1ea4e-140">Описание</span><span class="sxs-lookup"><span data-stu-id="1ea4e-140">Description</span></span> 
:------------ | :------------- 
**<span data-ttu-id="1ea4e-141">Name</span><span class="sxs-lookup"><span data-stu-id="1ea4e-141">Name</span></span>** | <span data-ttu-id="1ea4e-142">Имя и URL-путь запроса</span><span class="sxs-lookup"><span data-stu-id="1ea4e-142">Name and URL path of the request</span></span>
**<span data-ttu-id="1ea4e-143">Протокол</span><span class="sxs-lookup"><span data-stu-id="1ea4e-143">Protocol</span></span>** |  <span data-ttu-id="1ea4e-144">Тип протокола для запроса (например *, HTTPS, HTTP/2*)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-144">Type of protocol for the request (such as *HTTPS, HTTP/2*)</span></span>
**<span data-ttu-id="1ea4e-145">Метод</span><span class="sxs-lookup"><span data-stu-id="1ea4e-145">Method</span></span>** |    <span data-ttu-id="1ea4e-146">[Метод HTTP](https://developer.mozilla.org/docs/Web/HTTP/Methods) , используемый для запроса</span><span class="sxs-lookup"><span data-stu-id="1ea4e-146">[HTTP method](https://developer.mozilla.org/docs/Web/HTTP/Methods) used for the request</span></span>
**<span data-ttu-id="1ea4e-147">Результат</span><span class="sxs-lookup"><span data-stu-id="1ea4e-147">Result</span></span>** |    <span data-ttu-id="1ea4e-148">Код [состояния ответа HTTP](https://developer.mozilla.org/docs/Web/HTTP/Status)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-148">[HTTP response status](https://developer.mozilla.org/docs/Web/HTTP/Status)  code</span></span>
**<span data-ttu-id="1ea4e-149">Тип содержимого</span><span class="sxs-lookup"><span data-stu-id="1ea4e-149">Content type</span></span>** |  <span data-ttu-id="1ea4e-150">Тип запрашиваемого мультимедиа ([тип MIME](https://en.wikipedia.org/wiki/Media_type))</span><span class="sxs-lookup"><span data-stu-id="1ea4e-150">Type of media requested ([MIME type](https://en.wikipedia.org/wiki/Media_type))</span></span>
**<span data-ttu-id="1ea4e-151">Получено</span><span class="sxs-lookup"><span data-stu-id="1ea4e-151">Received</span></span>** | <span data-ttu-id="1ea4e-152">Размер ответа, доставленный сервером (не подсчитанный для кэшированных ответов)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-152">Size of the response as delivered by the server (not calculated for cached responses)</span></span>
**<span data-ttu-id="1ea4e-153">Время</span><span class="sxs-lookup"><span data-stu-id="1ea4e-153">Time</span></span>** |  <span data-ttu-id="1ea4e-154">Время для загрузки ответа сервера (не рассчитано для кэшированных ответов)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-154">Time to load the server response (not calculated for cached responses)</span></span>
**<span data-ttu-id="1ea4e-155">Владельцы</span><span class="sxs-lookup"><span data-stu-id="1ea4e-155">Initiator</span></span>** | <span data-ttu-id="1ea4e-156">Подсистема, отвечающая за инициирование запроса (например *, средство синтаксического анализа, перенаправление, сценарий и т*. д.)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-156">Subsystem responsible for initiating the request (such as *Parser, Redirect, Script, Other*)</span></span>
**<span data-ttu-id="1ea4e-157">Информация о сроках</span><span class="sxs-lookup"><span data-stu-id="1ea4e-157">Timeline</span></span>** | <span data-ttu-id="1ea4e-158">Визуальная временная шкала для сетевых событий запроса (например *, остановлена, разрешение (DNS), подключение (TCP), SSL, отправка, ожидание (TTFB), Загрузка*.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-158">Visual timeline for the network events of the request (such as *Stalled, Resolving(DNS), Connecting(TCP), SSL, Sending, Waiting(TTFB), Downloading*).</span></span> <span data-ttu-id="1ea4e-159">При наведении указателя мыши на диаграмму выводятся более детальные сведения о [времени](#timings)сетевого соединения.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-159">Hovering over the chart provides the more granular breakdown of network [network timings](#timings)).</span></span>

### <span data-ttu-id="1ea4e-160">Строка сводки</span><span class="sxs-lookup"><span data-stu-id="1ea4e-160">Summary bar</span></span>

<span data-ttu-id="1ea4e-161">В нижней части панели " **сеть** " выводятся общие сведения об ошибках сети HTTP, запросах, передаче данных и времени загрузки во время сеанса профилирования в сети (например, так как DevTools открыл и записывал сетевой трафик).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-161">The bar at the bottom of **Network** panel summarizes the total number of HTTP network errors, requests, data transfered, and load times during the network profiling session (i.e., since  DevTools were opened and recording network traffic).</span></span>

![Строка сводки по сети](./media/network_summary_bar.png)

<span data-ttu-id="1ea4e-163">**Затраченное время** указывает время между началом сеанса профилирования и моментом, когда последний ресурс был загружен из сети.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-163">**Elapsed time** means the time between the start of the profiling session and when the last resource was downloaded from the network.</span></span> <span data-ttu-id="1ea4e-164">Ресурсы, извлекаемые из кэша браузера, не начисляются время на этот номер.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-164">Resources fetched from the browser cache do not accrue time to this number.</span></span> 

<span data-ttu-id="1ea4e-165">**Время загрузки DOM** указывает время между началом сеанса профилирования и событием [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) , чтобы указать, что структура документа страницы была загружена и проанализирована (хотя и не обязательно какие-либо таблицы стилей, изображения или подкадры).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-165">**DOM load time** means the time between the start of the profiling session and when the [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) event was fired to indicate that the structure of the page document has been loaded and parsed (though not necessarily any stylesheets, images or subframes).</span></span>

<span data-ttu-id="1ea4e-166">Время **загрузки страницы** — это время между началом сеанса профилирования и событием [загрузки](https://developer.mozilla.org/docs/Web/Events/load) , чтобы показать, что документ страницы (и все его ресурсы) был полностью загружен.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-166">**Page load time** time means the time between the start of the profiling session and when the [load](https://developer.mozilla.org/docs/Web/Events/load) event was fired to indicate that the page document (and all its resources) has been fully loaded.</span></span>

## <span data-ttu-id="1ea4e-167">Сведения о запросе</span><span class="sxs-lookup"><span data-stu-id="1ea4e-167">Request details</span></span>

<span data-ttu-id="1ea4e-168">Если щелкнуть любой элемент в списке [**Сводка сети**](#network-summary) , откроется область [**сведения о запросе**](#request-details) с дополнительными сведениями на каждой из указанных ниже вкладок.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-168">Clicking on any entry in the [**Network summary**](#network-summary) list will open the [**Request details**](#request-details) pane with further information in each of the following tabs.</span></span>

![Область сведений о сетевом запросе](./media/network_request_details.png)

### <span data-ttu-id="1ea4e-170">Заголовки</span><span class="sxs-lookup"><span data-stu-id="1ea4e-170">Headers</span></span>
<span data-ttu-id="1ea4e-171">Показывает [заголовки HTTP](https://developer.mozilla.org/docs/Web/HTTP/Headers) , отправляемые на сервер и получаемые от него.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-171">Displays the [HTTP headers](https://developer.mozilla.org/docs/Web/HTTP/Headers) sent to and received from the server.</span></span> <span data-ttu-id="1ea4e-172">Щелкните правой кнопкой мыши любой элемент заголовка, чтобы скопировать его `Ctrl+C` в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-172">Right-click on any header entry to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="1ea4e-173">Вы также можете выбрать несколько элементов, удерживая нажатой `Shift` клавишу или выделить все ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-173">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="1ea4e-174">Body</span><span class="sxs-lookup"><span data-stu-id="1ea4e-174">Body</span></span>
<span data-ttu-id="1ea4e-175">Отображает данные основного текста (при их наличии) в полезных данных запроса и ответа.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-175">Displays the body data (if available) of the request and response payloads.</span></span>

<span data-ttu-id="1ea4e-176">Содержимое изображения отображается с помощью измерений и размера данных.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-176">Image content is displayed with dimensions and size data.</span></span>

<span data-ttu-id="1ea4e-177">Текстовое содержимое отображается в редакторе (только для чтения) с параметрами для форматирования minified содержимого с помощью **качественной печати** и (или) **переноса слов** для удобства чтения.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-177">Text content appears in a (read-only) editor with options to format minified content with **Pretty print** and/or **Word wrap** for easier readability.</span></span>

![Вкладка "текст" в области "сведения о запросе"](./media/network_details_body.png)

### <span data-ttu-id="1ea4e-179">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ea4e-179">Parameters</span></span>
<span data-ttu-id="1ea4e-180">Выводит параметры строки запроса на получение запросов GET.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-180">Displays query string parameters for GET requests.</span></span> <span data-ttu-id="1ea4e-181">Несмотря на то что параметры запросов POST отправляются в заголовках, запросы GET должны содержать их в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-181">While the parameters of POST requests are sent in the headers, GET requests include them in the URL.</span></span> <span data-ttu-id="1ea4e-182">Они разбиваются на эту ссылку для упрощения чтения.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-182">They're broken out here for easier reading.</span></span>

<span data-ttu-id="1ea4e-183">Щелкните правой кнопкой мыши любую строку, чтобы скопировать ее `Ctrl+C` в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-183">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="1ea4e-184">Вы также можете выбрать несколько элементов, удерживая нажатой `Shift` клавишу или выделить все ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-184">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="1ea4e-185">Файлы cookie</span><span class="sxs-lookup"><span data-stu-id="1ea4e-185">Cookies</span></span>
<span data-ttu-id="1ea4e-186">Отображение файлов cookie, которые отправляются и принимаются в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="1ea4e-186">Displays cookies that are sent or received as key/value pairs.</span></span>

<span data-ttu-id="1ea4e-187">Щелкните правой кнопкой мыши любую строку, чтобы скопировать ее `Ctrl+C` в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-187">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="1ea4e-188">Вы также можете выбрать несколько элементов, удерживая нажатой `Shift` клавишу или выделить все ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-188">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

<span data-ttu-id="1ea4e-189">Вы можете очистить сохраненные cookie-файлы для данного домена на [панели инструментов](#network-summary) (кнопка**Очистить "cookie** ").</span><span class="sxs-lookup"><span data-stu-id="1ea4e-189">You can clear the stored cookies for the given domain from the [Toolbar](#network-summary) (**Clear cookies** button).</span></span> 

### <span data-ttu-id="1ea4e-190">Времени показа</span><span class="sxs-lookup"><span data-stu-id="1ea4e-190">Timings</span></span>

<span data-ttu-id="1ea4e-191">Вкладка " **время** " содержит временную шкалу сетевых событий, связанных с загрузкой выбранного ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-191">The **Timings** tab provides a timeline of network events involved in the loading of the selected resource.</span></span> <span data-ttu-id="1ea4e-192">Это аналогично сведениям, находящихся в столбце *временная шкала* в [списке сетевых запросов](#network-request-list), но также включает события, ведущие к запросу, отправляемому по сети, например время ожидания (*остановлено*) в очереди запросов, разрешение DNS и установление соединения по протоколу TCP.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-192">This is similar to the information found in the *Timeline* column of the [Network request list](#network-request-list), but also includes the events leading up to the request being sent over the wire, such as time spent waiting (*Stalled*) in the request queue, DNS resolution, and establishing the TCP connection.</span></span> 

![Вкладка "время" в области "сведения о запросе"](./media/network_details_timings.png)

<span data-ttu-id="1ea4e-194">Помечаются перенаправления между другими ресурсами и нажатием ссылки в области [сведений о](#request details) сетевом запросе будет установлено фокус на этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-194">Redirections to/from other resources are noted, and clicking on the link will set focus to that resource in the network [request details](#request details) pane.</span></span>

<span data-ttu-id="1ea4e-195">Время задержки сети не влияет на ресурсы, загружаемые из кэша, поэтому не отображается диаграмма *синхронизации* сети.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-195">Resouces loaded from the cache are not affected by network latency, so no network *Timings* chart will display.</span></span>

![Перенаправленный ресурс, загруженный из кэша](./media/network_details_timings_cache_redirect.png)

<span data-ttu-id="1ea4e-197">Ниже указаны различные сетевые события, которые могут отображаться для определенного ресурса в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-197">Here are the different network events you might see for a given resource, in chronological order:</span></span>

#### <span data-ttu-id="1ea4e-198">Блокированы</span><span class="sxs-lookup"><span data-stu-id="1ea4e-198">Stalled</span></span>

<span data-ttu-id="1ea4e-199">Время, потраченное на ожидание доступа к сетевому подключению в очереди запросов.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-199">Time spent waiting for an available network connection in the request queue.</span></span> <span data-ttu-id="1ea4e-200">Для HTTP 1.0/1.1 Microsoft EDGE поддерживает не более шести (6) одновременных подключений TCP на каждое имя узла.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-200">For HTTP 1.0/1.1, Microsoft Edge allows a maximum of six (6) simultaneous TCP connections per hostname.</span></span> 

#### <span data-ttu-id="1ea4e-201">Разрешение (DNS)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-201">Resolving (DNS)</span></span>

<span data-ttu-id="1ea4e-202">Время, потраченное на поиск IP-адреса узла ресурса в DNS ([системе доменных имен](https://en.wikipedia.org/wiki/Domain_Name_System)).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-202">Time spent looking up the IP address for the hostname of the resource in the DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).</span></span>

#### <span data-ttu-id="1ea4e-203">Подключение (TCP)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-203">Connecting (TCP)</span></span>

<span data-ttu-id="1ea4e-204">Время, затраченное на установку соединения TCP ([протокол управления передачей](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-204">Time spent establishing the TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) connection.</span></span>

#### <span data-ttu-id="1ea4e-205">ТЕХНОЛОГИЮ</span><span class="sxs-lookup"><span data-stu-id="1ea4e-205">SSL</span></span>

<span data-ttu-id="1ea4e-206">Время, затраченное на согласование соединения SSL ([Secure Socket Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security)) с [прокси-сервером](https://en.wikipedia.org/wiki/Proxy_server) для узла.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-206">Time spent negotiating a SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security))  connection with the [proxy server](https://en.wikipedia.org/wiki/Proxy_server) for the host.</span></span>

#### <span data-ttu-id="1ea4e-207">Отправка</span><span class="sxs-lookup"><span data-stu-id="1ea4e-207">Sending</span></span>

<span data-ttu-id="1ea4e-208">Время, затраченное на отправку запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-208">Time spent sending the resource request.</span></span>

#### <span data-ttu-id="1ea4e-209">Ожидание (TTFB)</span><span class="sxs-lookup"><span data-stu-id="1ea4e-209">Waiting (TTFB)</span></span>

<span data-ttu-id="1ea4e-210">Время, потраченное на ожидание первого байта ответа от хост-сервера ("время до первого байта" или *TTFB*).</span><span class="sxs-lookup"><span data-stu-id="1ea4e-210">Time spent waiting for the first byte of the response from the host server ("time to first byte", or *TTFB*).</span></span>

#### <span data-ttu-id="1ea4e-211">Скачать</span><span class="sxs-lookup"><span data-stu-id="1ea4e-211">Downloading</span></span>

<span data-ttu-id="1ea4e-212">Время, потраченное на чтение ответа с сервера.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-212">Time spent reading the response from the server.</span></span>

## <span data-ttu-id="1ea4e-213">Горячие</span><span class="sxs-lookup"><span data-stu-id="1ea4e-213">Shortcuts</span></span>

| <span data-ttu-id="1ea4e-214">Действие</span><span class="sxs-lookup"><span data-stu-id="1ea4e-214">Action</span></span>                         | <span data-ttu-id="1ea4e-215">Появивше</span><span class="sxs-lookup"><span data-stu-id="1ea4e-215">Shortcut</span></span>     |
|:-------------------------------|:-------------|
| <span data-ttu-id="1ea4e-216">Запуск и остановка сеанса профилирования</span><span class="sxs-lookup"><span data-stu-id="1ea4e-216">Start / Stop profiling session</span></span> | `Ctrl` + `E` |
| <span data-ttu-id="1ea4e-217">Экспортировать как HAR</span><span class="sxs-lookup"><span data-stu-id="1ea4e-217">Export as HAR</span></span>                  | `Ctrl` + `S` |
| <span data-ttu-id="1ea4e-218">Поиск</span><span class="sxs-lookup"><span data-stu-id="1ea4e-218">Find</span></span>                           | `Ctrl` + `F` |
| <span data-ttu-id="1ea4e-219">Копировать</span><span class="sxs-lookup"><span data-stu-id="1ea4e-219">Copy</span></span>                           | `Ctrl` + `C` |

## <span data-ttu-id="1ea4e-220">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="1ea4e-220">Known Issues</span></span>

### <span data-ttu-id="1ea4e-221">Не удалось запустить агент сетевого семейства.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-221">The network collection agent failed to start.</span></span>

<span data-ttu-id="1ea4e-222">Если отображается это сообщение об ошибке: **агенту сетевого семейства сети не удалось запустить** средство "сеть", выполните указанные ниже действия, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-222">If you see this error message: **The network collection agent failed to start** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="1ea4e-223">Нажмите клавишу `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="1ea4e-223">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="1ea4e-224">В диалоговом окне Выполнить введите **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-224">In the Run dialog, enter **services.msc**.</span></span>
![Известные проблемы – 1](./media/known_issues_1.PNG)

3. <span data-ttu-id="1ea4e-226">Найдите **стандартную службу сборщика центра диагностики Microsoft (R)** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-226">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![Известные проблемы – 2](./media/known_issues_2.PNG)

4. <span data-ttu-id="1ea4e-228">Перезапустите **стандартную службу сборщика центра диагностики Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-228">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![Известные проблемы – 3](./media/known_issues_3.PNG)

5. <span data-ttu-id="1ea4e-230">Закройте инструменты разработчика Microsoft EDGE и вкладку. Откройте новую вкладку, перейдите на нужную страницу и нажмите клавишу `F12` .</span><span class="sxs-lookup"><span data-stu-id="1ea4e-230">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="1ea4e-231">Теперь вы должны увидеть индикатор воспроизведения рядом с командой **сеть** и сетевые запросы для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-231">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![Известные проблемы — 4](./media/known_issues_4-network.PNG)

<span data-ttu-id="1ea4e-233">Вы по-прежнему столкнулись с проблемами?</span><span class="sxs-lookup"><span data-stu-id="1ea4e-233">Still running into problems?</span></span> <span data-ttu-id="1ea4e-234">Пожалуйста, отправьте нам свой отзыв с помощью значка " **Отправить отзыв** "!</span><span class="sxs-lookup"><span data-stu-id="1ea4e-234">Please send us your feedback using the **Send feedback** icon!</span></span> 

![Известные проблемы – 5](./media/known_issues_5.PNG)

### <span data-ttu-id="1ea4e-236">Не удалось остановить агент сетевого семейства.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-236">The network collection agent failed to stop.</span></span>

<span data-ttu-id="1ea4e-237">Если отображается это сообщение об ошибке: **не удалось остановить агент сетевого сбора** в инструменте "сеть", выполните указанные ниже действия, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-237">If you see this error message: **The network collection agent failed to stop** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="1ea4e-238">Нажмите клавишу `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="1ea4e-238">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="1ea4e-239">В диалоговом окне Выполнить введите **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-239">In the Run dialog, enter **services.msc**.</span></span>
![Известные проблемы – 1](./media/known_issues_1.PNG)

3. <span data-ttu-id="1ea4e-241">Найдите **стандартную службу сборщика центра диагностики Microsoft (R)** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-241">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![Известные проблемы – 2](./media/known_issues_2.PNG)

4. <span data-ttu-id="1ea4e-243">Перезапустите **стандартную службу сборщика центра диагностики Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-243">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![Известные проблемы – 3](./media/known_issues_3.PNG)

5. <span data-ttu-id="1ea4e-245">Закройте инструменты разработчика Microsoft EDGE и вкладку. Откройте новую вкладку, перейдите на нужную страницу и нажмите клавишу `F12` .</span><span class="sxs-lookup"><span data-stu-id="1ea4e-245">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="1ea4e-246">Теперь вы должны увидеть индикатор воспроизведения рядом с командой **сеть** и сетевые запросы для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="1ea4e-246">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![Известные проблемы — 4](./media/known_issues_4-network.PNG)

<span data-ttu-id="1ea4e-248">Вы по-прежнему столкнулись с проблемами?</span><span class="sxs-lookup"><span data-stu-id="1ea4e-248">Still running into problems?</span></span> <span data-ttu-id="1ea4e-249">Пожалуйста, отправьте нам свой отзыв с помощью значка " **Отправить отзыв** "!</span><span class="sxs-lookup"><span data-stu-id="1ea4e-249">Please send us your feedback using the **Send feedback** icon!</span></span> 

![Известные проблемы – 5](./media/known_issues_5.PNG)

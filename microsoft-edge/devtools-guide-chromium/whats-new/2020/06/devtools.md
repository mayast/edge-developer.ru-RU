---
title: Новые возможности DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7b0193d25fb1d081e5746ec1271ca7b9f4e60c23
ms.sourcegitcommit: ad5eb43172280974b8c063867c2097f7c5c0e77d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2020
ms.locfileid: "10898313"
---
# <span data-ttu-id="3485f-103">Новые возможности DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="3485f-103">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="3485f-104">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3485f-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="3485f-105">В следующих разделах представлен список извещений, которые могут быть пропущены командой Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3485f-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="3485f-106">Просмотрите объявления, чтобы ознакомиться с новыми возможностями в DevTools, в расширениях кода VS и т. д.</span><span class="sxs-lookup"><span data-stu-id="3485f-106">See the announcements to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="3485f-107">Чтобы всегда оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Microsoft Edge DevTools Team для Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="3485f-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="3485f-108">Функции отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="3485f-108">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3485f-110">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3485f-110">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-111">Группа Microsoft Edge DevTools — совместная работа с группой Chrome DevTools и Chromium, чтобы добавить в DevTools новые функции отладки сетки каскадных стилей.</span><span class="sxs-lookup"><span data-stu-id="3485f-111">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="3485f-112">Теперь вы можете отображать номера линий сетки, зазоры сетки и дополнительные линии сетки в качестве наложений на страницы.</span><span class="sxs-lookup"><span data-stu-id="3485f-112">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="3485f-113">Кроме того, в скором времени становятся более улучшены инструменты сетки.</span><span class="sxs-lookup"><span data-stu-id="3485f-113">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Функции отладки сетки каскадных стилей" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="3485f-115">Функции отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="3485f-115">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3485f-116">Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить новые возможности отладки сетки каскадных стилей**.</span><span class="sxs-lookup"><span data-stu-id="3485f-116">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="3485f-117">Чтобы опробовать эксперимент с образцом, ознакомьтесь со статьей [Пример планировщика сетки каскадных стилей][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="3485f-117">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="3485f-118">[#1047356][CR1047356] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-118">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="3485f-119">Изменение и повторное воспроизведение запросов с помощью сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="3485f-119">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3485f-121">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3485f-121">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-122">Теперь вы можете использовать команду " **изменить и воспроизвести** " на запросах в [сетевом журнале][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**.</span><span class="sxs-lookup"><span data-stu-id="3485f-122">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Изменение и повторное воспроизведение запроса в NetworkLog с помощью сетевой консоли" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="3485f-124">Изменение и повторное воспроизведение запроса в [NetworkLog][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**</span><span class="sxs-lookup"><span data-stu-id="3485f-124">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-125">Новая панель, **Сетевая консоль** открывается в [ящике DevTools][DevtoolsCustomizeIndexDrawer] и автоматически заполняется данными для HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="3485f-125">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="3485f-126">Чтобы просмотреть ответ, возвращенный сервером, измените запрос и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3485f-126">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="3485f-127">Вы также можете использовать **консоль сети** для создания и отправки HTTP-запросов непосредственно из DevTools.</span><span class="sxs-lookup"><span data-stu-id="3485f-127">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Панель "Сетевая консоль"" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="3485f-129">Панель " **Сетевая консоль** "</span><span class="sxs-lookup"><span data-stu-id="3485f-129">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="3485f-130">Чтобы увидеть **сетевую консоль** в главной панели \ (Top \), а не в [DevTools][DevtoolsCustomizeIndexDrawer], ознакомьтесь с разделами [Перемещение инструментов между панелями](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="3485f-130">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="3485f-131">Чтобы включить эксперимент, ознакомьтесь со следующей командой [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить сетевую консоль**.</span><span class="sxs-lookup"><span data-stu-id="3485f-131">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="3485f-132">Откройте [Журнал сети][DevtoolsNetworkIndexLogActivity], откройте контекстное меню (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="3485f-132">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="3485f-133">[#1093687][CR1093687] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-133">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="3485f-134">События respondWith рабочего процесса на вкладке время</span><span class="sxs-lookup"><span data-stu-id="3485f-134">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="3485f-135">Вкладка **время** на панели " **сеть** " теперь включает `respondWith` события рабочих процессов служб.</span><span class="sxs-lookup"><span data-stu-id="3485f-135">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="3485f-136">`respondWith`Событие "сотрудник службы" показывает продолжительность, начиная с момента, `fetch` когда обработчик событий сотрудника службы начнет выполняться до того момента, когда `respondWith` `fetch` будет сопоставлено обещание обработчика.</span><span class="sxs-lookup"><span data-stu-id="3485f-136">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Событие "Рабочий процесс службы respondWith" на вкладке "время" на панели "сеть"" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="3485f-138">`respondWith`Событие "сотрудник службы" на вкладке " **время** " на панели " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="3485f-138">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-139">Развернутый **ответ получен** , чтобы просмотреть дополнительные сведения из `fetch` ответа, например, `CacheStorageCacheName` `serviceWorkerResponseSource` и `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="3485f-139">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Получен ответ на запрос Expand для просмотра дополнительных сведений из ответа на выборку" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="3485f-141">**Получен ответ на запрос** Expand для просмотра дополнительных сведений из `fetch` ответа</span><span class="sxs-lookup"><span data-stu-id="3485f-141">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-142">[#1066579][CR1066579] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-142">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="3485f-143">Обратная связь по этой подсказке на панели "вопросы"</span><span class="sxs-lookup"><span data-stu-id="3485f-143">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3485f-145">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3485f-145">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-146">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для обеспечения специальных возможностей, совместимости, безопасности, производительности, PWAs и других распространенных проблем, возникающих при работе в Интернете.</span><span class="sxs-lookup"><span data-stu-id="3485f-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="3485f-147">Теперь вы можете увидеть отзыв по этой подсказке на панели " [вопросы][DevtoolsIssues] ".</span><span class="sxs-lookup"><span data-stu-id="3485f-147">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="3485f-149">Обратная связь по этой подсказке на панели "вопросы"</span><span class="sxs-lookup"><span data-stu-id="3485f-149">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3485f-150">Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить подсказку**.</span><span class="sxs-lookup"><span data-stu-id="3485f-150">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="3485f-151">Откройте панель " [проблемы][DevtoolsIssues] ", чтобы увидеть отзыв из подсказки.</span><span class="sxs-lookup"><span data-stu-id="3485f-151">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="3485f-152">[#1070378][CR1070378] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-152">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="3485f-153">Перемещение инструментов между панелями</span><span class="sxs-lookup"><span data-stu-id="3485f-153">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3485f-155">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3485f-155">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-156">Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3485f-156">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="3485f-157">Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3485f-157">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="3485f-158">Теперь вы можете настраивать макет DevTools, перемещая инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="3485f-158">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="3485f-160">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="3485f-160">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3485f-161">Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить функцию поддержки для перемещения вкладок между панелями**.</span><span class="sxs-lookup"><span data-stu-id="3485f-161">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="3485f-162">[#897944][CR897944] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-162">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="3485f-163">Улучшенная всплывающая подсказка инициатора на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="3485f-163">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="3485f-164">В Microsoft Edge 83 и 84 с помощью всплывающих подсказок для столбца инициаторов, в котором отображается причина запроса ресурсов, в [сетевом журнале][DevtoolsNetworkIndexLogActivity] отображается горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="3485f-164">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="3485f-165">Вы можете видеть стек вызовов, который инициировал запрос, прокручивать по горизонтали в подсказке.</span><span class="sxs-lookup"><span data-stu-id="3485f-165">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Всплывающая подсказка инициатора в Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="3485f-167">Всплывающая подсказка инициатора в Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="3485f-167">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-168">Начиная с Microsoft Edge 85, теперь вы можете видеть стек вызовов инициаторов в подсказке без горизонтальной прокрутки.</span><span class="sxs-lookup"><span data-stu-id="3485f-168">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Всплывающая подсказка инициатора в Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="3485f-170">Всплывающая подсказка инициатора в Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="3485f-170">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="3485f-171">[#1069404][CR1069404] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-171">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="3485f-172">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-172">Announcements from the Chromium project</span></span>  

<span data-ttu-id="3485f-173">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 85, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="3485f-173">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="3485f-174">Редактирование стилей для платформ CSS в JS</span><span class="sxs-lookup"><span data-stu-id="3485f-174">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="3485f-175">Панель " **стили** " теперь обеспечивает улучшенную поддержку редактирования стилей, созданных с помощью API [объектной модели CSS (CSSOM)][CsswgDraftsCssom] .</span><span class="sxs-lookup"><span data-stu-id="3485f-175">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="3485f-176">Во многих платформах и библиотеках, использующих CSS из JS, для конструирования стилей используются API CSSOM в разделе "внутри".</span><span class="sxs-lookup"><span data-stu-id="3485f-176">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="3485f-177">Теперь вы можете изменять стили, добавленные в JavaScript с помощью [построенных таблиц стилей][WicgConstructStylesheet].</span><span class="sxs-lookup"><span data-stu-id="3485f-177">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="3485f-178">Создаваемые таблицы стилей — это новый способ создания и распространения многократно используемых стилей при использовании [теневой модели DOM][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="3485f-178">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="3485f-179">Например, стили, `h1` добавленные с помощью `CSSStyleSheet` \ (CSSOM API \), не были изменены ранее.</span><span class="sxs-lookup"><span data-stu-id="3485f-179">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="3485f-180">Теперь стили доступны для редактирования в области **стили** .</span><span class="sxs-lookup"><span data-stu-id="3485f-180">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Изменение свойства Background для стилей H1, добавленных с CSSStyleSheet из розового в LightBlue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="3485f-182">Изменение `background` свойства `h1` стиля, добавленного в значение `CSSStyleSheet` FROM `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="3485f-182">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="3485f-183">Придайте этой функции [пример с использованием CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="3485f-183">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="3485f-184">[#946975][CR946975] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-184">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="3485f-185">Lighthouse 6 на панели Lighthouse</span><span class="sxs-lookup"><span data-stu-id="3485f-185">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="3485f-186">Панель **Lighthouse** теперь работает под управлением Lighthouse 6.</span><span class="sxs-lookup"><span data-stu-id="3485f-186">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="3485f-187">Полный список всех изменений можно найти в разделе [заметки о выпуске 6.0.0][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="3485f-187">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="3485f-188">Lighthouse 6,0 предлагает три новые метрики для отчета: самую крупную краску \ (LCP \), интегральная схема сдвига \ (CLS \) и общее время блокировки \ (TBT \).</span><span class="sxs-lookup"><span data-stu-id="3485f-188">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="3485f-189">Формула оценки производительности также была изменена в соответствии с тем, чтобы лучше понять процесс загрузки пользователя.</span><span class="sxs-lookup"><span data-stu-id="3485f-189">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="3485f-190">[#772558][CR772558] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-190">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="3485f-191">Устаревшее изображение для первого осмысленного изображения</span><span class="sxs-lookup"><span data-stu-id="3485f-191">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="3485f-192">Первый значащий графический редактор (FMP \ "\" \ "\") устарел в Lighthouse 6,0.</span><span class="sxs-lookup"><span data-stu-id="3485f-192">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="3485f-193">FMP также был удален из панели **Performance** .</span><span class="sxs-lookup"><span data-stu-id="3485f-193">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="3485f-194">**Самая крупная краска с содержимым** — Рекомендуемая замена для fmp.</span><span class="sxs-lookup"><span data-stu-id="3485f-194">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="3485f-195">[#1096008][CR1096008] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-195">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="3485f-196">Поддержка новых функций JavaScript</span><span class="sxs-lookup"><span data-stu-id="3485f-196">Support for new JavaScript features</span></span>  

<span data-ttu-id="3485f-197">В DevTools теперь улучшена поддержка некоторых последних языковых функций JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3485f-197">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="3485f-198">[Необязательное автозавершение цепочки цепочек][V8DevOptionalChaining]</span><span class="sxs-lookup"><span data-stu-id="3485f-198">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3485f-199">Автоматическое завершение свойств в **консоли** теперь поддерживает дополнительный синтаксис цепочек, например `name?.` теперь он работает и в дополнение к нему `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="3485f-199">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="3485f-200">Подсветка синтаксиса для [закрытых полей][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="3485f-200">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3485f-201">закрытые поля класса теперь правильно выделены синтаксисом и печатаются на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="3485f-201">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="3485f-202">Выделение синтаксиса для [непустого оператора слияния][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="3485f-202">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3485f-203">DevTools правильно — печатает на панели « **источники** » оператор объединения без значений NULL.</span><span class="sxs-lookup"><span data-stu-id="3485f-203">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="3485f-204">Проблемы с Chromium [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="3485f-204">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="3485f-205">Новые предупреждения о сочетаниях клавиш для приложения в области манифеста</span><span class="sxs-lookup"><span data-stu-id="3485f-205">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="3485f-206">**Сочетания клавиш** для работы с приложениями помогают пользователям быстро запускать наиболее распространенные или Рекомендуемые задачи в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="3485f-206">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="3485f-207">В области **манифеста** отображаются предупреждения для указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="3485f-207">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="3485f-208">Значки сочетаний клавиш приложения меньше 96x96 пикселей</span><span class="sxs-lookup"><span data-stu-id="3485f-208">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="3485f-209">Значки сочетаний клавиш приложения и манифеста не квадратны \ (так как значки игнорируются)</span><span class="sxs-lookup"><span data-stu-id="3485f-209">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Предупреждения о сочетаниях клавиш для приложения" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="3485f-211">Предупреждения о сочетаниях клавиш для приложения</span><span class="sxs-lookup"><span data-stu-id="3485f-211">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-212">[#955497][CR955497] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-212">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="3485f-213">Последовательная отображение вычисляемой области</span><span class="sxs-lookup"><span data-stu-id="3485f-213">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="3485f-214">**Вычисляемая** область на панели " **элементы** " теперь отображается единообразно в виде области на всех размерах окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="3485f-214">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="3485f-215">Ранее **Вычисляемая** область была объединена в области " **стили** ", когда ширина окна просмотра DevTools была узкой.</span><span class="sxs-lookup"><span data-stu-id="3485f-215">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Вычисляемая область последовательно отображается как отдельная область, даже если DevTools узким" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="3485f-217">**Вычисляемая** область последовательно отображается как отдельная область, даже если DevTools узким.</span><span class="sxs-lookup"><span data-stu-id="3485f-217">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="3485f-218">[#1073899][CR1073899] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-218">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="3485f-219">Смещения байт-кода для файлов сборки</span><span class="sxs-lookup"><span data-stu-id="3485f-219">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="3485f-220">DevTools теперь использует смещения байт-кода для отображения номеров строк Wasm дизассемблированного кода.</span><span class="sxs-lookup"><span data-stu-id="3485f-220">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="3485f-221">Номера строк упрощают просмотр двоичных данных и более последовательную работу, так как среда выполнения Wasm ссылается на расположение.</span><span class="sxs-lookup"><span data-stu-id="3485f-221">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="3485f-222">[#1071432][CR1071432] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-222">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="3485f-223">Построчное копирование и вырезание на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="3485f-223">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="3485f-224">При копировании или вырезании без выделения в [редакторе палитры «источники][DevtoolsSourcesEditCssJavascript]» DevTools копирует или вырезает текущую строку содержимого.</span><span class="sxs-lookup"><span data-stu-id="3485f-224">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="С курсором в конце строки 5 копируется вся строка из pen.js в DevTools и вставляется в код VS." lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="3485f-226">С курсором в конце строки 5 копируется вся строка из **pen.js** в DevTools и вставляется в [код VS][VSCode].</span><span class="sxs-lookup"><span data-stu-id="3485f-226">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [VS Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="3485f-227">[#800028][CR800028] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-227">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="3485f-228">Обновления параметров консоли</span><span class="sxs-lookup"><span data-stu-id="3485f-228">Console Settings updates</span></span>  

#### <span data-ttu-id="3485f-229">Разгруппирование одинаковых сообщений консоли</span><span class="sxs-lookup"><span data-stu-id="3485f-229">Ungroup same console messages</span></span>  

<span data-ttu-id="3485f-230">Для повторяющихся сообщений **Группа одинаковый** переключатель в разделе Параметры консоли будет применена.</span><span class="sxs-lookup"><span data-stu-id="3485f-230">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="3485f-231">Ранее она была применена к аналогичным сообщениям.</span><span class="sxs-lookup"><span data-stu-id="3485f-231">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="3485f-232">Например, ранее DevTools не разгруппирование сообщений, несмотря на то, что `hello` флажок **Group похоже** не установлен.</span><span class="sxs-lookup"><span data-stu-id="3485f-232">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="3485f-233">Теперь `hello` сообщения разгруппированы.</span><span class="sxs-lookup"><span data-stu-id="3485f-233">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Если флажок "Группировать" не установлен, сообщения приветствия разгруппированы не будут" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="3485f-235">Если флажок **Группировка** не установлен, `hello` сообщения разносятся в разгруппирование.</span><span class="sxs-lookup"><span data-stu-id="3485f-235">When **Group similar** is unchecked, the `hello` messages are ungrouped.</span></span>
:::image-end:::  

<span data-ttu-id="3485f-236">Придайте этой функции [пример, который отправляет на консоль повторяющиеся сообщения][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="3485f-236">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="3485f-237">[#1082963][CR1082963] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-237">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="3485f-238">Сохранение только выбранных контекстных параметров</span><span class="sxs-lookup"><span data-stu-id="3485f-238">Persisting Selected context only settings</span></span>  

<span data-ttu-id="3485f-239">**Выбранный контекст** теперь сохраняется только в параметрах консоли.</span><span class="sxs-lookup"><span data-stu-id="3485f-239">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="3485f-240">Ранее параметры были сброшены каждый раз при закрытии и повторном открытии DevTools.</span><span class="sxs-lookup"><span data-stu-id="3485f-240">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="3485f-241">Изменение приводит к поведению параметров с другими параметрами консоли.</span><span class="sxs-lookup"><span data-stu-id="3485f-241">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Параметр "только выбранный контекст"" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="3485f-243">Параметр " **только выбранный контекст** "</span><span class="sxs-lookup"><span data-stu-id="3485f-243">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-244">[#1055875][CR1055875] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-244">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="3485f-245">Обновления панели "производительность"</span><span class="sxs-lookup"><span data-stu-id="3485f-245">Performance panel updates</span></span>  

#### <span data-ttu-id="3485f-246">Информация кэша компиляции для JavaScript на панели "производительность"</span><span class="sxs-lookup"><span data-stu-id="3485f-246">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="3485f-247">[Данные кэша компиляции для JavaScript][V8DevCodeCaching] теперь всегда отображаются на вкладке "Сводка" на панели "производительность".</span><span class="sxs-lookup"><span data-stu-id="3485f-247">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="3485f-248">Ранее DevTools не показывает ничего, связанного с кэшированием кода, если кэширование кода не произошло.</span><span class="sxs-lookup"><span data-stu-id="3485f-248">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Данные кэша компиляции для JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="3485f-250">Данные кэша компиляции для JavaScript</span><span class="sxs-lookup"><span data-stu-id="3485f-250">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-251">[#912581][CR912581] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-251">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="3485f-252">Выравнивание времени навигации на панели «производительность»</span><span class="sxs-lookup"><span data-stu-id="3485f-252">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="3485f-253">Панель **производительности** , используемая для отображения времени на линейках на основе начала записи.</span><span class="sxs-lookup"><span data-stu-id="3485f-253">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="3485f-254">Время ожидания изменилось для записей, в которых пользователь осуществляет переход, где DevTools теперь показывает время линейки относительно навигации.</span><span class="sxs-lookup"><span data-stu-id="3485f-254">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Выравнивание времени навигации на панели «производительность»" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="3485f-256">Выравнивание времени навигации на панели « **производительность** »</span><span class="sxs-lookup"><span data-stu-id="3485f-256">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-257">Время, для которого `DOMContentLoaded` Первая краска, первая краска и наибольшее количество событий, связанных с содержимым, обновляется в соответствии с началом навигации, а это значит, что время соответствует значению времени, указанное в `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="3485f-257">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="3485f-258">[#974550][CR974550] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-258">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="3485f-259">Новые значки для точек останова, условных точек останова и logpoints</span><span class="sxs-lookup"><span data-stu-id="3485f-259">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="3485f-260">На панели « **источники** » есть новые дизайны для точек останова, условных точек останова и logpoints.</span><span class="sxs-lookup"><span data-stu-id="3485f-260">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="3485f-261">Точки останова представлены на красном круге, точно так же, как и в случае с [кодом][VSCode] и [Visual Studio][VS].</span><span class="sxs-lookup"><span data-stu-id="3485f-261">Breakpoints are represented by a red circle, just like [VS Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="3485f-262">Значки добавляются для различения условных точек останова и logpoints.</span><span class="sxs-lookup"><span data-stu-id="3485f-262">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Точки останова" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="3485f-264">Точки останова</span><span class="sxs-lookup"><span data-stu-id="3485f-264">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="3485f-265">[#1041830][CR1041830] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="3485f-265">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="3485f-266">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3485f-266">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="3485f-267">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="3485f-267">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="3485f-268">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="3485f-268">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="3485f-269">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="3485f-269">Getting in touch with Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="3485f-270">Следующие параметры позволяют обсуждать новые возможности и изменения в записи, а также любые другие связанные с DevTools.</span><span class="sxs-lookup"><span data-stu-id="3485f-270">Use the following options to discuss the new features and changes in the post, or anything else related to DevTools.</span></span>  

* <span data-ttu-id="3485f-271">Отправка отзыва с помощью значка **обратной связи** в DevTools</span><span class="sxs-lookup"><span data-stu-id="3485f-271">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
* <span data-ttu-id="3485f-272">Твит на [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="3485f-272">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
* <span data-ttu-id="3485f-273">Отправка предложения в [Вебе][TheWebWeWant]</span><span class="sxs-lookup"><span data-stu-id="3485f-273">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
* <span data-ttu-id="3485f-274">Ошибка "файл" на этой странице в репозитории " [Edge — разработчик][GitHubMicrosoftDocsEdgeDeveloperNewIssue] "</span><span class="sxs-lookup"><span data-stu-id="3485f-274">File bugs on this page in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="Значок обратной связи в Microsoft Edge DevTools" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  <span data-ttu-id="3485f-276">Значок **обратной связи** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3485f-276">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включите экспериментальные функции — экспериментальные функции | Документы Microsoft"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Общие сведения об панели редактирования CSS и JavaScript-sources | Документы Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Регистрация активности сети — проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Редактирование стилей для платформ CSS-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Отправлять повторяющиеся сообщения на консоль | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Пример планировщика сетки CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии Lighthouse | Ошибки Chromium"  
[CR800028]: https://crbug.com/800028 "Повторяющийся ярлык строки в редакторе средств разработчика не работает после обновления Chrome | Ошибки Chromium"  
[CR912581]: https://crbug.com/912581 "Предоставление сценариев, которые были бы кэшированы в коде с помощью V8 в DevTools/about: Tracing | Ошибки Chromium"  
[CR946975]: https://crbug.com/946975 "Боковая панель "стили DevTools" не работает с сконструированными таблицами стилей | Ошибки Chromium"  
[CR955497]: https://crbug.com/955497 "Контекстное меню значка приложения для PWAs | Ошибки Chromium"  
[CR974550]: https://crbug.com/974550 "Несоответствие метрик между панелью производительности и performanceObserver | Ошибки Chromium"  
[CR1041830]: https://crbug.com/1041830 "Улучшение цветопередачи для точек останова | Ошибки Chromium"  
[CR1055875]: https://crbug.com/1055875 "Значение выбранного контекста параметр консоли не сохраняется после закрытия и повторного открытия средств разработчика | Ошибки Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Показать ServiceWorkers выбор временной шкалы для запроса на панели "сеть" | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Базовые возможности для разработчиков Wasm | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "вычисляемый стиль" исчезает в режиме отклика | Ошибки Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: выделение синтаксических конструкций не работает с закрытыми полями | Ошибки Chromium"  
[CR1082963]: https://crbug.com/1082963 "Не удается отключить поведение группировки аналогичных сообщений в консоли | Ошибки Chromium"  
[CR1083214]: https://crbug.com/1083214 "Acorn не поддерживает дополнительное объединение | Ошибки Chromium"  
[CR1083797]: https://crbug.com/1083797 "Неправильное распечатка для ненулевого объединения | Ошибки Chromium"  
[CR1096008]: https://crbug.com/1096008 "Удалить FMP | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Сетка CSS/гибкая таблица/подсказка для таблиц | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Инструмент "создать" для создания и воспроизведения запросов виртуальных сетей | Ошибки Chromium"  
[CR1070378]: https://crbug.com/1070378 "Интегрировать подсказку в DevTools | Ошибки Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Средства разработки] всплывающие элементы мини-приложения слишком узкие | Ошибки Chromium"  
[CR897944]: https://crbug.com/897944 "Перетаскиваемые панели DevTool | Ошибки Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Использование теневой модели DOM | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Каналы предварительной версии Microsoft Edge"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Код Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Объектная модель CSS (CSSOM) | Черновики редакторов рабочих групп W3C CSS"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Закрытые поля класса — открытые и закрытые поля класса | V8. Разработки"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Кэширование кода для разработчиков JavaScript | V8. Разработки"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Ненулевое объединение | V8. Разработки"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Дополнительные сцепления | V8. Разработки"  

[WebhintMain]: https://webhint.io "Подсказка"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Объекты стилей, которые вы создаете? Веб-Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Требуемый веб-сайт"  

> [!NOTE]
> <span data-ttu-id="3485f-325">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3485f-325">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3485f-326">Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/06/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="3485f-326">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3485f-328">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3485f-328">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

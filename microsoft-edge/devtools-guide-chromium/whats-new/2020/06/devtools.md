---
title: Новые возможности в DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f569414a95336278c93b1bbafd57153ca902df12
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942192"
---
# <span data-ttu-id="7eba1-103">Новые возможности средств разработчиков (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="7eba1-103">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="7eba1-104">Объявления от команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7eba1-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="7eba1-105">В следующих разделах приведен список извещений, которые вы можете пропустить от команды разработчиков Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7eba1-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="7eba1-106">Ознакомьтесь с извещениями о новых возможностях DevTools, расширениях кода VS и других возможностях.</span><span class="sxs-lookup"><span data-stu-id="7eba1-106">See the announcements to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="7eba1-107">Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge и][MicrosoftEdgePreviewChannels] [подписайтесь на группу Microsoft Edge DevTools в Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="7eba1-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="7eba1-108">Возможности отладки CSS-таблицы</span><span class="sxs-lookup"><span data-stu-id="7eba1-108">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   <span data-ttu-id="7eba1-110">Экспертальные возможности</span><span class="sxs-lookup"><span data-stu-id="7eba1-110">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-111">Команда разработчиков Microsoft Edge DevTools работает в месте совместного использования Chrome DevTools и Chromium для добавления новых функций отладки CSS в разработчики CSS.</span><span class="sxs-lookup"><span data-stu-id="7eba1-111">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="7eba1-112">Теперь вы можете отображать номера линий сетки, государственные и расширенные линии сетки в виде наложения.</span><span class="sxs-lookup"><span data-stu-id="7eba1-112">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="7eba1-113">Кроме того, в ближайшее время инструменты сетки станут доступны в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="7eba1-113">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Возможности отладки CSS-таблицы" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="7eba1-115">Возможности отладки CSS-таблицы</span><span class="sxs-lookup"><span data-stu-id="7eba1-115">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7eba1-116">Чтобы включить эксперты, см. [раздел "Включение эксперальных возможностей"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок "Включить новые функции отладки **CSS".**</span><span class="sxs-lookup"><span data-stu-id="7eba1-116">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="7eba1-117">Ознакомиться с примером экспертов с примером см. в примере [планировщика CSS.][CodepenRachelweilYzwBzKM]</span><span class="sxs-lookup"><span data-stu-id="7eba1-117">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="7eba1-118">Проблема с chromium [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="7eba1-118">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="7eba1-119">Изменение и воспроизведение запросов с помощью сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="7eba1-119">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   <span data-ttu-id="7eba1-121">Экспертальные возможности</span><span class="sxs-lookup"><span data-stu-id="7eba1-121">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-122">Теперь вы можете использовать команду "Изменить **и** воспроизвести воспроизведение при запросах в [сетевом журнале"][DevtoolsNetworkIndexLogActivity] с **помощью сетевой консоли.**</span><span class="sxs-lookup"><span data-stu-id="7eba1-122">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Изменение и воспроизведение запроса в сети NetworkLog с помощью консоли Network" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="7eba1-124">Изменение и воспроизведение запроса в [сети NetworkLog][DevtoolsNetworkIndexLogActivity] с **помощью консоли Network**</span><span class="sxs-lookup"><span data-stu-id="7eba1-124">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-125">В средстве рисования [DevTools][DevtoolsCustomizeIndexDrawer] откроется панель "Сетевой консоль" и автоматически замещаются сведениями для HTTP-запроса. **Network Console**</span><span class="sxs-lookup"><span data-stu-id="7eba1-125">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="7eba1-126">Чтобы просмотреть ответ, возвращенный с сервера, отредактировайте запрос \(при необходимости\) и нажмите **кнопку "Отправить".**</span><span class="sxs-lookup"><span data-stu-id="7eba1-126">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="7eba1-127">Сетевая **консоль** также можно использовать для создания и отправки HTTP-запросов непосредственно в средствах разработки.</span><span class="sxs-lookup"><span data-stu-id="7eba1-127">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Панель "Сетевая консоль"" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="7eba1-129">Панель **"Сетевая консоль"**</span><span class="sxs-lookup"><span data-stu-id="7eba1-129">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="7eba1-130">Чтобы **просмотреть консоль сети** в основной области \(верхний\) панель \(верхний\) панель [devTools—][DevtoolsCustomizeIndexDrawer]см. инструменты перемещения между [панелями.](#move-tools-between-panels)</span><span class="sxs-lookup"><span data-stu-id="7eba1-130">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="7eba1-131">Чтобы включить эксперт, см. [раздел "Включение эксперальных функций"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **"Включить сетевую консоль".**</span><span class="sxs-lookup"><span data-stu-id="7eba1-131">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="7eba1-132">Откройте [контекстное][DevtoolsNetworkIndexLogActivity]меню, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **команду "Изменить и воспроизвести".**</span><span class="sxs-lookup"><span data-stu-id="7eba1-132">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="7eba1-133">Проблема с #1093687 chromium [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="7eba1-133">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="7eba1-134">На вкладке "Время" в личной службе отвечают на сообщения о работе службы</span><span class="sxs-lookup"><span data-stu-id="7eba1-134">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="7eba1-135">Вкладка **"Время показа** слайдов" на **панели** network теперь содержит события `respondWith` работников служб.</span><span class="sxs-lookup"><span data-stu-id="7eba1-135">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="7eba1-136">Событие работника службы отображает срок от времени непосредственного обработчика работника службы до начала его работы с временем, когда устанавливается минимум `respondWith` `fetch` диспетчера `respondWith` `fetch` обработчика.</span><span class="sxs-lookup"><span data-stu-id="7eba1-136">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Событие процедуры обслуживания на вкладке "Время" панели сети" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="7eba1-138">Событие `respondWith` работника службы на вкладке **"Время показа** слайдов" **панели сети**</span><span class="sxs-lookup"><span data-stu-id="7eba1-138">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-139">Разверните **полученный ответ, чтобы** просмотреть дополнительные сведения от `fetch` `CacheStorageCacheName` ответа, `serviceWorkerResponseSource` например, `ResponseTime` и.</span><span class="sxs-lookup"><span data-stu-id="7eba1-139">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Разверните полученный ответ, чтобы просмотреть дополнительные сведения от удаленного ответа" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="7eba1-141">Развернуть **полученный ответ, чтобы** просмотреть дополнительные сведения `fetch` от ответа</span><span class="sxs-lookup"><span data-stu-id="7eba1-141">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-142">Проблема с chromium [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="7eba1-142">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="7eba1-143">отзыв ы веб-сайта в панели "Проблемы"</span><span class="sxs-lookup"><span data-stu-id="7eba1-143">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   <span data-ttu-id="7eba1-145">Экспертальные возможности</span><span class="sxs-lookup"><span data-stu-id="7eba1-145">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-146">[webhint][WebhintMain] — это открытый инструмент, в котором вы восприятие удобства использования, совместимости, безопасности, производительности, PWA и других проблем разработки веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="7eba1-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="7eba1-147">Теперь вы можете просмотреть отзывы веб-хранилища на [панели "Проблемы".][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="7eba1-147">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="отзыв ы веб-сайта в панели "Проблемы"" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="7eba1-149">отзыв ы веб-сайта в панели "Проблемы"</span><span class="sxs-lookup"><span data-stu-id="7eba1-149">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7eba1-150">Чтобы включить эксперт, см. [статью "Включение эксперальных возможностей"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **"Включить веб-хороший веб-сайт".**</span><span class="sxs-lookup"><span data-stu-id="7eba1-150">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="7eba1-151">Откройте [панель "Вопросы"][DevtoolsIssues] для просмотра отзывов веб-хорошего трудозатрат.</span><span class="sxs-lookup"><span data-stu-id="7eba1-151">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="7eba1-152">Проблема с [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="7eba1-152">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="7eba1-153">Перемещение инструментов между панелями</span><span class="sxs-lookup"><span data-stu-id="7eba1-153">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспертальные возможности":::
   <span data-ttu-id="7eba1-155">Экспертальные возможности</span><span class="sxs-lookup"><span data-stu-id="7eba1-155">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-156">Как обычно, такие инструменты, **Elements** как **Network** Элементы и сеть, могут открываться только в основной панели \(верхней\) панели разработчиков.</span><span class="sxs-lookup"><span data-stu-id="7eba1-156">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="7eba1-157">Аналогичным причиной таких инструментов, как трехмерное представление и проблемы, можно открыть только в панели \(нижнь\)) панели Средств Разработчиков. **3D View** **Issues**</span><span class="sxs-lookup"><span data-stu-id="7eba1-157">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="7eba1-158">Теперь вы можете настраивать макет DevTools путем перемещения инструментов между верхними и нижними панелями.</span><span class="sxs-lookup"><span data-stu-id="7eba1-158">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="7eba1-160">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="7eba1-160">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7eba1-161">Чтобы включить эксперт, см. [раздел "Включить экспертные функции"][DevtoolsExperimentalFeaturesTurnOn] и установите флажок "Разрешить поддержку" для перемещения **вкладок между панелями.**</span><span class="sxs-lookup"><span data-stu-id="7eba1-161">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="7eba1-162">Проблема с [хромом#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="7eba1-162">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="7eba1-163">Улучшенная подсказка инициатора на панели сети</span><span class="sxs-lookup"><span data-stu-id="7eba1-163">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="7eba1-164">В Microsoft Edge 83 и 84 подсказки для столбца "Инициатор" для [Network Log][DevtoolsNetworkIndexLogActivity] столбца "Инициатор" с отображением причины запроса ресурса на сетевом журнале с горизонтальной полосой прокрутки.</span><span class="sxs-lookup"><span data-stu-id="7eba1-164">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="7eba1-165">Вы сможете видеть только стопку звонков, инициировавшую запрос, прокрутив горизонтально в подсказке.</span><span class="sxs-lookup"><span data-stu-id="7eba1-165">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Подсказка инициатора в Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="7eba1-167">Подсказка инициатора в Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="7eba1-167">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-168">Начиная с Microsoft Edge 85, теперь вы можете увидеть стек нужда ть инициатор звонков сигнала в подсказке без прокрутки по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="7eba1-168">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Подсказка инициатора в Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="7eba1-170">Подсказка инициатора в Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="7eba1-170">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="7eba1-171">Проблема с #1069404 chromium [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="7eba1-171">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="7eba1-172">Извещения из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="7eba1-172">Announcements from the Chromium project</span></span>  

<span data-ttu-id="7eba1-173">В следующих разделах описаны дополнительные функции, доступные в Microsoft Edge 85, которые были внесены в проект Chromium.</span><span class="sxs-lookup"><span data-stu-id="7eba1-173">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="7eba1-174">Редактирование стилей для структур структур CSS в JSS</span><span class="sxs-lookup"><span data-stu-id="7eba1-174">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="7eba1-175">В **области "Стили"** теперь можно изменять стили, созданные с помощью API-объектной модели [CSS (CSSOM).][CsswgDraftsCssom]</span><span class="sxs-lookup"><span data-stu-id="7eba1-175">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="7eba1-176">Многие из них инфраструктуры и библиотеки CSS используют API CSSOM под разработчиками.</span><span class="sxs-lookup"><span data-stu-id="7eba1-176">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="7eba1-177">Теперь можно изменять стили, добавленные в JavaScript, с помощью [конструкции стилей.][WicgConstructStylesheet]</span><span class="sxs-lookup"><span data-stu-id="7eba1-177">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="7eba1-178">Конструктивные стили — это новый способ создания и распространения стилей повторно используемых стилей при использовании [тени DOM.][MdnShadowDom]</span><span class="sxs-lookup"><span data-stu-id="7eba1-178">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="7eba1-179">Например, `h1` добавленные стили с `CSSStyleSheet` \(CSSOM\) не редактирулись ранее.</span><span class="sxs-lookup"><span data-stu-id="7eba1-179">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="7eba1-180">Теперь стили можно изменять в области **"Стили".**</span><span class="sxs-lookup"><span data-stu-id="7eba1-180">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Изменение свойства фона для стилей h1, добавленных с помощью розовой таблицы на светлый" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="7eba1-182">`background`Измените свойство `h1` стилей, добавленных `CSSStyleSheet` в `pink` `lightblue` список.</span><span class="sxs-lookup"><span data-stu-id="7eba1-182">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="7eba1-183">Попробовать эту функцию [с образцом, использующим CSS-семи.][CodepenZoherghadyaliAbdgrpz]</span><span class="sxs-lookup"><span data-stu-id="7eba1-183">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="7eba1-184">Проблема с [#946975][CR946975] хромеум#946975</span><span class="sxs-lookup"><span data-stu-id="7eba1-184">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="7eba1-185">Lighthouse 6 на панели "Молния"</span><span class="sxs-lookup"><span data-stu-id="7eba1-185">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="7eba1-186">Панель **"Молуль"** теперь работает на десяти чужих десятках.</span><span class="sxs-lookup"><span data-stu-id="7eba1-186">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="7eba1-187">Полный список всех изменений см. в [заметках о выпуске 6.0.0.][GithubGoogleChromeLighthouse600]</span><span class="sxs-lookup"><span data-stu-id="7eba1-187">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="7eba1-188">В отчет включены три новых показателя: самый большой объем контента: самый большой объем контента (LCP\),интегральная смена макета Shift \(CLS\) и общее время блокирования времени \(TBT\).</span><span class="sxs-lookup"><span data-stu-id="7eba1-188">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="7eba1-189">Формула оценки производительности также была удалена, чтобы лучше отразить нагрузку пользователя.</span><span class="sxs-lookup"><span data-stu-id="7eba1-189">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="7eba1-190">Проблема с [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="7eba1-190">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="7eba1-191">First Meaningful Paint</span><span class="sxs-lookup"><span data-stu-id="7eba1-191">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="7eba1-192">Первая понятная paint \(FMP\) устарела в Lighthouse 6.0.</span><span class="sxs-lookup"><span data-stu-id="7eba1-192">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="7eba1-193">FMP также удален с панели **производительности.**</span><span class="sxs-lookup"><span data-stu-id="7eba1-193">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="7eba1-194">**Самый большой объем контента —** рекомендуемый заменой для FMP.</span><span class="sxs-lookup"><span data-stu-id="7eba1-194">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="7eba1-195">Проблема с [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="7eba1-195">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="7eba1-196">Поддержка новых функций JavaScript</span><span class="sxs-lookup"><span data-stu-id="7eba1-196">Support for new JavaScript features</span></span>  

<span data-ttu-id="7eba1-197">Теперь В DevTools теперь поддерживается поддержка некоторых последних функций языков JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7eba1-197">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="7eba1-198">[Необязательное][V8DevOptionalChaining] автозавершение синтаксиса</span><span class="sxs-lookup"><span data-stu-id="7eba1-198">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7eba1-199">Автозавершение свойств в консоли теперь поддерживает необязательный синтаксис цепочки цепочки, **Console** `name?.` `name.` например `name[` и.</span><span class="sxs-lookup"><span data-stu-id="7eba1-199">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="7eba1-200">Выделение синтаксиса для [частных полей][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="7eba1-200">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7eba1-201">частные поля класса теперь выделяются правильно, а на **панели источников выделяются прежние** поля.</span><span class="sxs-lookup"><span data-stu-id="7eba1-201">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="7eba1-202">Выделение синтаксиса [для оператора нули][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="7eba1-202">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7eba1-203">Средства Разработки теперь правильно распечатываются оператор ы операционных шифров абсоллийских операций, на **панели "Источники".**</span><span class="sxs-lookup"><span data-stu-id="7eba1-203">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7eba1-204">Проблемы с [хроме#1073903][CR1073903] [#1083797][CR1083797] #1083214, [#1083797][CR1083214]</span><span class="sxs-lookup"><span data-stu-id="7eba1-204">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="7eba1-205">Предупреждения о новых сочетаниях клавиш приложения в области манифеста</span><span class="sxs-lookup"><span data-stu-id="7eba1-205">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="7eba1-206">**Сочетания клавиш для приложений** помогают пользователям быстро начинать типичные или рекомендуемые задачи в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="7eba1-206">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="7eba1-207">В **области манифеста** теперь отображаются предупреждения для перечисленных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="7eba1-207">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="7eba1-208">Значки сочетаний клавиш приложений меньше 96 x 96 пикселей</span><span class="sxs-lookup"><span data-stu-id="7eba1-208">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="7eba1-209">Значки ярлыков приложений и манифеста не являются квадратными \(так как значки игнорируются\)</span><span class="sxs-lookup"><span data-stu-id="7eba1-209">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Предупреждения о сочетаниях клавиш приложений" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="7eba1-211">Предупреждения о сочетаниях клавиш приложений</span><span class="sxs-lookup"><span data-stu-id="7eba1-211">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-212">Проблема с chromium [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="7eba1-212">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="7eba1-213">Единообразный экран области вычисляемой области</span><span class="sxs-lookup"><span data-stu-id="7eba1-213">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="7eba1-214">В **области "Элементы"** панель "Элементы" похожна на единообразный список областей просмотра. **Elements**</span><span class="sxs-lookup"><span data-stu-id="7eba1-214">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="7eba1-215">Ранее, **ранее** созданная в области **"Стили"** в области "Стили" при уменьшении ширины представления DevTools.</span><span class="sxs-lookup"><span data-stu-id="7eba1-215">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Вырезанная область вычисляется постоянно, даже если область "Разработчики" уже сужат" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="7eba1-217">**Вырезанная область вычисляется** постоянно, даже если узкие для devTools сужаются.</span><span class="sxs-lookup"><span data-stu-id="7eba1-217">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="7eba1-218">Проблема с [#1073899][CR1073899] хромеум#1073899</span><span class="sxs-lookup"><span data-stu-id="7eba1-218">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="7eba1-219">Смещение байтов для файлов WebAssembly</span><span class="sxs-lookup"><span data-stu-id="7eba1-219">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="7eba1-220">В DevTools теперь используются смещения байтов для отображения чисел строк, которые были интегрированы с еженедельными.</span><span class="sxs-lookup"><span data-stu-id="7eba1-220">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="7eba1-221">Номера строк делают более четкими, что просматриваетданное двоичные данные и более единообразие использования ссылок на расположения пользователя Временных шкалах.</span><span class="sxs-lookup"><span data-stu-id="7eba1-221">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="7eba1-222">Проблема с [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="7eba1-222">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="7eba1-223">Построчная копирование и вырезание в области источников</span><span class="sxs-lookup"><span data-stu-id="7eba1-223">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="7eba1-224">При копировании или вырезании без выделения в редакторе источников [не][DevtoolsSourcesEditCssJavascript]выбрано, средства DevTools копируют или вырезают текущую строку содержимого.</span><span class="sxs-lookup"><span data-stu-id="7eba1-224">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="При нажатии указателя в конце строки 5 скопируйте всю строку pen.js в devTools и вставьте в код VS-код VS." lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="7eba1-226">Скопируйте строку изpen.jsв **средствах** разработчиков и вставьте [в код VS код VS.][VSCode]</span><span class="sxs-lookup"><span data-stu-id="7eba1-226">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [VS Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="7eba1-227">Проблема с #800028 Chromium [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="7eba1-227">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="7eba1-228">Обновления параметров консоли</span><span class="sxs-lookup"><span data-stu-id="7eba1-228">Console Settings updates</span></span>  

#### <span data-ttu-id="7eba1-229">Разгруппирование сообщений в консоли</span><span class="sxs-lookup"><span data-stu-id="7eba1-229">Ungroup same console messages</span></span>  

<span data-ttu-id="7eba1-230">Параметр **"Группа"** так же, как и в параметрах консоли, теперь применяется для дублированных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eba1-230">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="7eba1-231">Ранее применяется к похожим сообщениям.</span><span class="sxs-lookup"><span data-stu-id="7eba1-231">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="7eba1-232">Например, ранее devTools не разгруппировал сообщения, хотя похожие на `hello` группы снят. **Group similar**</span><span class="sxs-lookup"><span data-stu-id="7eba1-232">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="7eba1-233">Теперь сообщения `hello` будут разгруппированы.</span><span class="sxs-lookup"><span data-stu-id="7eba1-233">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Если группа желаемых снята, сообщения приветствия разгруппируются" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="7eba1-235">Если **похожие флажки** сняты, сообщения `hello` будут отменены.</span><span class="sxs-lookup"><span data-stu-id="7eba1-235">When **Group similar** is unchecked, the `hello` messages are ungrouped.</span></span>
:::image-end:::  

<span data-ttu-id="7eba1-236">Попробуйте эту функцию использовать [образец, который отправляет дублирующиеся сообщения в консоль.][CodepenZoherghadyaliZyrjgdJ]</span><span class="sxs-lookup"><span data-stu-id="7eba1-236">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="7eba1-237">Проблема с [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="7eba1-237">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="7eba1-238">Параметры постоянного контекста</span><span class="sxs-lookup"><span data-stu-id="7eba1-238">Persisting Selected context only settings</span></span>  

<span data-ttu-id="7eba1-239">**Выбранный контекст меню** не удаляется.</span><span class="sxs-lookup"><span data-stu-id="7eba1-239">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="7eba1-240">Ранее параметры были сброшены каждый раз при закрытии и повторном открытии DevTools.</span><span class="sxs-lookup"><span data-stu-id="7eba1-240">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="7eba1-241">Изменение вносит изменения в настройки согласованно с другими параметрами консоли.</span><span class="sxs-lookup"><span data-stu-id="7eba1-241">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Только выбранный контекст" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="7eba1-243">**Только выбранный контекст**</span><span class="sxs-lookup"><span data-stu-id="7eba1-243">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-244">Проблема с [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="7eba1-244">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="7eba1-245">Обновления панели производительности</span><span class="sxs-lookup"><span data-stu-id="7eba1-245">Performance panel updates</span></span>  

#### <span data-ttu-id="7eba1-246">Информация о кэше компиляции для JavaScript на панели производительности</span><span class="sxs-lookup"><span data-stu-id="7eba1-246">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="7eba1-247">[Информация о кэше компиляции JavaScript][V8DevCodeCaching] теперь всегда отображается на вкладке "Сводка" панели быстродействия.</span><span class="sxs-lookup"><span data-stu-id="7eba1-247">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="7eba1-248">Ранее в DevTools не было относительно кэширования кода ничего, связанное с кэшированием кода.</span><span class="sxs-lookup"><span data-stu-id="7eba1-248">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Кэш съемки для JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="7eba1-250">Кэш съемки для JavaScript</span><span class="sxs-lookup"><span data-stu-id="7eba1-250">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-251">Проблема с [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="7eba1-251">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="7eba1-252">Выравнивание время переходов на панели производительности</span><span class="sxs-lookup"><span data-stu-id="7eba1-252">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="7eba1-253">На **панели "Производительность"** отображаются временные шкалы на линейках в зависимости от времени начала записи.</span><span class="sxs-lookup"><span data-stu-id="7eba1-253">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="7eba1-254">Теперь время показа теперь изменилась при переходе по записям, когда пользователь переходит по интерфейсу DevTools теперь отображает таймер таймер относительно навигации.</span><span class="sxs-lookup"><span data-stu-id="7eba1-254">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Выравнивание временных показаслайд по навигации на панели performance" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="7eba1-256">Выравнивание временных показаслайд по навигации **на панели performance**</span><span class="sxs-lookup"><span data-stu-id="7eba1-256">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-257">Время, продолжительная первая рисованная питание, первый контент и крупный контент, обновляются относительно начала навигации, то есть соответствует время показа `DOMContentLoaded` `PerformanceObserver` слайдов, полученным.</span><span class="sxs-lookup"><span data-stu-id="7eba1-257">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="7eba1-258">Проблема с #974550 chromium [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="7eba1-258">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="7eba1-259">Новые значки для разбиения точек, условных точек и логических точек</span><span class="sxs-lookup"><span data-stu-id="7eba1-259">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="7eba1-260">В **области "Источники"** добавлены новые макеты разбивки, условных точек и логических точек.</span><span class="sxs-lookup"><span data-stu-id="7eba1-260">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="7eba1-261">Разрывы представлены красными кружками, как [и код VS-][VSCode] [и Visual Studio.][VS]</span><span class="sxs-lookup"><span data-stu-id="7eba1-261">Breakpoints are represented by a red circle, just like [VS Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="7eba1-262">Значки добавляются к различные условные точки и логические точки.</span><span class="sxs-lookup"><span data-stu-id="7eba1-262">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Точки останова" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="7eba1-264">Точки останова</span><span class="sxs-lookup"><span data-stu-id="7eba1-264">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="7eba1-265">Проблема с #1041830 chromium [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="7eba1-265">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="7eba1-266">Загрузить каналы с предварительными версиями Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7eba1-266">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="7eba1-267">Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7eba1-267">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="7eba1-268">Каналы с предварительными версиями доступны новейшие функции Разработчиков.</span><span class="sxs-lookup"><span data-stu-id="7eba1-268">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="7eba1-269">Совместная работа с помощью команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7eba1-269">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (на базе Chromium) | Документы Майкрософт"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Команды меню "Запуск" в меню Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Рисование — настройка средств разработчиков Microsoft Edge | Документы Майкрософт"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включение экспертальных функций — экспертальные функции | Документы Майкрософт"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Поиск и устранение проблем с средством разработчиков Microsoft Edge | Документы Майкрософт"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Edit CSS and JavaScript — Обзор панели источников | Документы Майкрософт"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Журнал действий с сетью: проверка действий с ее сетью в средствах разработки Microsoft Edge | Документы Майкрософт"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Редактирование стилей для структур в CSS -in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Отправка дубликатов сообщений на консоль | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Пример планировщика CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки на Chromium"  

[CR772558]: https://crbug.com/772558 "Разработчики: обновление до последней версии Lighthouse | Ошибки на Chromium"  
[CR800028]: https://crbug.com/800028 "После обновления Chrome ярлык строки в редакторе средств разработчика не работают? Ошибки на Chromium"  
[CR912581]: https://crbug.com/912581 "Выводит ся, какие сценарии были кэшированы кодированным кодом V8 в DevTools/about:tracing | Ошибки на Chromium"  
[CR946975]: https://crbug.com/946975 "Боковая панель Разработчиков не работает со структурированными таблицами стилей | Ошибки на Chromium"  
[CR955497]: https://crbug.com/955497 "Контекстное меню значка приложения для PWA | Ошибки на Chromium"  
[CR974550]: https://crbug.com/974550 "Несоответствие между панелью Perf и PerformanceObserver | Ошибки на Chromium"  
[CR1041830]: https://crbug.com/1041830 "Улучшены цвета разбивки | Ошибки на Chromium"  
[CR1055875]: https://crbug.com/1055875 "Значение выбранной консоли не удаляется после закрытия и повторного открытия средств разработчика | Ошибки на Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: показать временную шкалу служб fetch TimeLine на запрос на панели Network | Ошибки на Chromium"  
[CR1071432]: https://crbug.com/1071432 "Были опытные возможности для разработчиков | Ошибки на Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "Вычисляемый стиль" исчезает в режиме респондента | Ошибки на Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: выделение синтаксиса не работает с частными полями | Ошибки на Chromium"  
[CR1082963]: https://crbug.com/1082963 "Невозможно отключить поведение групп ых поведения консоли | Ошибки на Chromium"  
[CR1083214]: https://crbug.com/1083214 "Acorn не поддерживает дополнительную цепочку цепочки | Ошибки на Chromium"  
[CR1083797]: https://crbug.com/1083797 "Напечатать неработающую печать для необычных количества шифрования | Ошибки на Chromium"  
[CR1096008]: https://crbug.com/1096008 "Удалить FMP | Ошибки на Chromium"  
[CR1047356]: https://crbug.com/1047356 "Сетка CSS, Flexbox/инструменты таблиц | Ошибки на Chromium"  
[CR1093687]: https://crbug.com/1093687 "Создание средства для создания и повторного синтаксиса синтаксических запросов | Ошибки на Chromium"  
[CR1070378]: https://crbug.com/1070378 "Интеграция веб-страниц в DevTools | Ошибки на Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Средства разработки] Всплывающие мини-приложения слишком узкими | Ошибки на Chromium"  
[CR897944]: https://crbug.com/897944 "Панели разработчиков | Ошибки на Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "версии 6.0.0–GoogleChrome/lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая проблема: MicrosoftDocs/edge-разработчики"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Использование тени DOM | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Каналы предварительной версии Microsoft Edge"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Visual Studio код"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Объектную модель CSS (CSSOM) | Редактор черновиков группы CSS working Group"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools твиттер"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Частные поля класса — поля "Общие" и "Частное занятие" | 8. Разработка"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Кэширование кодов для разработчиков JavaScript | 8. Разработка"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Неульзя производить необычный количество | 8. Разработка"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Необязательное цепочка | 8. Разработка"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Объекты конструктивной таблицы стилей | Web Incubator CG"

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

[TheWebWeWant]: https://webwewant.fyi/ "Нужный веб-час"  

> [!NOTE]
> <span data-ttu-id="7eba1-318">Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]</span><span class="sxs-lookup"><span data-stu-id="7eba1-318">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7eba1-319">Исходная страница [here](https://developers.google.com/web/updates/2020/06/devtools/index) найдена и находится в динамическом оси Игнатьельской ориентации, и она разрабатывается [Деконом][JecelynYeen] \(Разработчик, Разработчик, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="7eba1-319">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="7eba1-321">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7eba1-321">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

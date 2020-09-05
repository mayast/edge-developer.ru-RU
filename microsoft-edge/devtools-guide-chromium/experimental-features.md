---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: a5793b6f4b67add313958ad4b8cee01cb7b09dbf
ms.sourcegitcommit: 7e3644e6b1d568ab795168e421c013814efa0073
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/04/2020
ms.locfileid: "10996161"
---
# <span data-ttu-id="8e541-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="8e541-104">Experimental features</span></span>  

<span data-ttu-id="8e541-105">Вы можете использовать экспериментальные функции, которые все еще находятся на стадии разработки в Microsoft Edge DevTools для тестирования и [предоставления отзывов](#providing-feedback-on-experimental-features) , прежде чем они будут выпущены широко.</span><span class="sxs-lookup"><span data-stu-id="8e541-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="8e541-106">Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.</span><span class="sxs-lookup"><span data-stu-id="8e541-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="8e541-107">Включение экспериментальных функций</span><span class="sxs-lookup"><span data-stu-id="8e541-107">Turn on experimental features</span></span>  

<span data-ttu-id="8e541-108">Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8e541-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="8e541-109">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="8e541-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="8e541-110">Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="8e541-110">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="8e541-111">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="8e541-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="8e541-112">Открытие области [параметров][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="8e541-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="8e541-113">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="8e541-113">Select `Shift`+`?`.</span></span>  <span data-ttu-id="8e541-114">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="8e541-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="8e541-115">В левой части области **параметров** выберите раздел **эксперименты** .</span><span class="sxs-lookup"><span data-stu-id="8e541-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="8e541-117">Список экспериментов в параметрах DevTools</span><span class="sxs-lookup"><span data-stu-id="8e541-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8e541-118">На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажки рядом с функциями, которые нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="8e541-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="8e541-119">Закройте и снова откройте Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="8e541-120">Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="8e541-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="8e541-121">Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="8e541-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="8e541-122">Выделены экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="8e541-122">Highlighted experimental features</span></span>  

<span data-ttu-id="8e541-123">В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8e541-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="8e541-124">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="8e541-124">Experimental feature</span></span> | <span data-ttu-id="8e541-125">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8e541-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="8e541-126">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="8e541-126">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="8e541-127">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="8e541-127">85 or later</span></span> |  
| [<span data-ttu-id="8e541-128">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="8e541-128">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="8e541-129">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="8e541-129">85 or later</span></span> |  
| [<span data-ttu-id="8e541-130">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="8e541-130">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="8e541-131">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="8e541-131">85 or later</span></span> |  
| [<span data-ttu-id="8e541-132">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="8e541-132">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="8e541-133">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="8e541-133">85 or later</span></span> |  
| [<span data-ttu-id="8e541-134">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="8e541-134">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="8e541-135">86 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="8e541-135">86 or later</span></span> |  

### <span data-ttu-id="8e541-136">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="8e541-136">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="8e541-137">Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="8e541-137">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="8e541-138">Вы можете настроить перекрытия в DevTools параметров.</span><span class="sxs-lookup"><span data-stu-id="8e541-138">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="8e541-140">Функция отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="8e541-140">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8e541-141">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="8e541-141">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="8e541-142">Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-142">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="8e541-143">Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-143">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="8e541-144">Если вы выберете эксперимент, вы можете перемещать инструменты между верхней и нижней панелями, наведя указатель мыши на вкладку, открыв контекстное меню, а затем выбрав пункты **переместить в начало** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="8e541-144">When you choose the experiment, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="8e541-145">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-145">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="8e541-146">Чтобы отобразить или скрыть нижнюю панель, нажмите кнопку `Escape` .</span><span class="sxs-lookup"><span data-stu-id="8e541-146">To show or hide the bottom panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="8e541-148">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="8e541-148">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8e541-149">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="8e541-149">Enable webhint</span></span>  

<span data-ttu-id="8e541-150">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для обеспечения специальных возможностей, совместимости, безопасности, производительности, PWAs и других распространенных проблем, возникающих при работе в Интернете.</span><span class="sxs-lookup"><span data-stu-id="8e541-150">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="8e541-151">При [эксперименте с DevTools][WebhintMain] на панели " [вопросы][DevtoolsIssues] " появляется обратная связь с помощью подсказки.</span><span class="sxs-lookup"><span data-stu-id="8e541-151">The [webhint][WebhintMain] experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="8e541-152">Вы можете выбрать проблему, чтобы получить сведения о том, как устранить проблему и список уязвимых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="8e541-152">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="8e541-153">Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-153">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="8e541-155">Обратная связь по этой подсказке на панели " **вопросы** "</span><span class="sxs-lookup"><span data-stu-id="8e541-155">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8e541-156">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="8e541-156">Enable Network Console</span></span>  

<span data-ttu-id="8e541-157">**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e541-157">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="8e541-158">Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.</span><span class="sxs-lookup"><span data-stu-id="8e541-158">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="8e541-159">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-159">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="8e541-160">Чтобы использовать консоль "сеть", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8e541-160">To use the Network Console:</span></span>  

1.  <span data-ttu-id="8e541-161">Открытие области " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="8e541-161">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="8e541-162">Найдите сетевой запрос, который вы хотите изменить и отправить повторно.</span><span class="sxs-lookup"><span data-stu-id="8e541-162">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="8e541-163">Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="8e541-163">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="8e541-164">Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="8e541-164">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="8e541-165">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="8e541-165">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.png" alt-text="Сетевая консоль в консольном ящике" lightbox="./media/network-network-console.png":::
   <span data-ttu-id="8e541-167">**Сетевая консоль** в **консольном** ящике</span><span class="sxs-lookup"><span data-stu-id="8e541-167">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### <span data-ttu-id="8e541-168">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="8e541-168">Enable Source Order Viewer</span></span>  

<span data-ttu-id="8e541-169">**Средство просмотра исходного порядка** — это рабочее название эксперимента для отображения порядка элементов в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="8e541-169">**Source Order Viewer** is the working title of an experiment to display the order of elements in the page source.</span></span>  <span data-ttu-id="8e541-170">Вы можете использовать **средство просмотра заказов исходного кода** для поиска проблем с читаемостью на страницах, так как порядок отображения на экране может отличаться от порядка источника, который в противном случае будет обладать предохранителями для пользователей средства чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="8e541-170">You may use the **Source Order Viewer** experiment to find accessibility issues in your pages since the display order on-screen may differ from the order of the source, which confuses screen reader users.</span></span>  

<span data-ttu-id="8e541-171">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-171">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="8e541-172">Чтобы использовать средство просмотра заказов исходного кода, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8e541-172">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="8e541-173">Откройте область **элементы** .</span><span class="sxs-lookup"><span data-stu-id="8e541-173">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="8e541-174">Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).</span><span class="sxs-lookup"><span data-stu-id="8e541-174">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="8e541-175">В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .</span><span class="sxs-lookup"><span data-stu-id="8e541-175">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="8e541-176">Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="8e541-176">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Средство просмотра исходного порядка на панели "Специальные возможности"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="8e541-178">**Средство просмотра исходного порядка** на панели " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="8e541-178">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="8e541-179">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="8e541-179">Previous experimental features</span></span>  

*   <span data-ttu-id="8e541-180">Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="8e541-180">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="8e541-181">[Настройка сочетаний клавиш][DevtoolsCustomKeyboardShortcuts] теперь доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="8e541-181">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>
## <span data-ttu-id="8e541-182">Отзывы о экспериментальных функциях</span><span class="sxs-lookup"><span data-stu-id="8e541-182">Providing feedback on experimental features</span></span>  

<span data-ttu-id="8e541-183">Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e541-183">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="8e541-184">Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools</span><span class="sxs-lookup"><span data-stu-id="8e541-184">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="8e541-185">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="8e541-185">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>   

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="8e541-187">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8e541-187">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[WebhintMain]: https://webhint.io "Подсказка" 

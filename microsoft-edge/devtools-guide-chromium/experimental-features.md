---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: 4915c909921bb4c5eaa8d727ab7a08493b941445
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986124"
---
# <span data-ttu-id="5535d-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="5535d-104">Experimental features</span></span>  

<span data-ttu-id="5535d-105">Вы можете использовать экспериментальные функции, которые все еще находятся на стадии разработки в Microsoft Edge DevTools для тестирования и [предоставления отзывов](#providing-feedback-on-experimental-features) , прежде чем они будут выпущены широко.</span><span class="sxs-lookup"><span data-stu-id="5535d-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="5535d-106">Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.</span><span class="sxs-lookup"><span data-stu-id="5535d-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="5535d-107">Включение экспериментальных функций</span><span class="sxs-lookup"><span data-stu-id="5535d-107">Turn on experimental features</span></span>  

<span data-ttu-id="5535d-108">Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5535d-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="5535d-109">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="5535d-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="5535d-110">Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="5535d-110">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="5535d-111">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="5535d-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="5535d-112">Открытие области [параметров][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="5535d-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="5535d-113">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="5535d-113">Select `Shift`+`?`.</span></span>  <span data-ttu-id="5535d-114">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="5535d-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="5535d-115">В левой части области **параметров** выберите раздел **эксперименты** .</span><span class="sxs-lookup"><span data-stu-id="5535d-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="5535d-117">Список экспериментов в параметрах DevTools</span><span class="sxs-lookup"><span data-stu-id="5535d-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5535d-118">На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажки рядом с функциями, которые нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="5535d-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="5535d-119">Закройте и снова откройте Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="5535d-120">Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="5535d-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="5535d-121">Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="5535d-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="5535d-122">Выделены экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="5535d-122">Highlighted experimental features</span></span>  

<span data-ttu-id="5535d-123">В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5535d-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="5535d-124">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="5535d-124">Experimental feature</span></span> | <span data-ttu-id="5535d-125">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5535d-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="5535d-126">Вкладка "Включение настраиваемых сочетаний клавиш"</span><span class="sxs-lookup"><span data-stu-id="5535d-126">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="5535d-127">84 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="5535d-127">84 or later</span></span> |
| [<span data-ttu-id="5535d-128">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="5535d-128">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="5535d-129">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="5535d-129">85 or later</span></span> |  
| [<span data-ttu-id="5535d-130">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="5535d-130">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="5535d-131">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="5535d-131">85 or later</span></span> |  
| [<span data-ttu-id="5535d-132">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="5535d-132">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="5535d-133">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="5535d-133">85 or later</span></span> |  
| [<span data-ttu-id="5535d-134">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="5535d-134">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="5535d-135">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="5535d-135">85 or later</span></span> |  
| [<span data-ttu-id="5535d-136">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="5535d-136">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="5535d-137">86 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="5535d-137">86 or later</span></span> |  

### <span data-ttu-id="5535d-138">Вкладка "Включение настраиваемых сочетаний клавиш"</span><span class="sxs-lookup"><span data-stu-id="5535d-138">Enable custom keyboard shortcuts settings tab</span></span>  

<span data-ttu-id="5535d-139">Эта страница содержит новую страницу " **ярлыки** " в [параметрах DevTools][DevToolsCustomizeSettings] , которая позволяет использовать соответствующие [сочетания клавиш][DevToolsShortcuts] в DevTools с [кодом Microsoft Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="5535d-139">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] that enables matching [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  

<span data-ttu-id="5535d-140">После включения эксперимента снова откройте [Параметры DevTools][DevToolsCustomizeSettings] с помощью SELECT `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="5535d-140">Once you have enabled the experiment, open [DevTools Settings][DevToolsCustomizeSettings] again using select `Shift`+`?`.</span></span>  <span data-ttu-id="5535d-141">Перейдите на страницу новые **сочетания клавиш** .</span><span class="sxs-lookup"><span data-stu-id="5535d-141">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="5535d-142">Выберите **DevTools (по умолчанию)** в раскрывающемся списке **искать сочетания клавиш из предварительной настройки** и выберите **код Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="5535d-142">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="5535d-143">Сочетания клавиш в DevTools теперь соответствуют сочетаниям клавиш для эквивалентных действий в коде Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5535d-143">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="./media/experiments-keyboard-shortcut.png":::
   <span data-ttu-id="5535d-145">Соответствие сочетаний клавиш в DevTools с кодом Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5535d-145">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="5535d-146">Например, в Windows для приостановки или продолжения выполнения сценария в [Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] используется сочетание клавиш `F5` .</span><span class="sxs-lookup"><span data-stu-id="5535d-146">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="5535d-147">В стиле **DevTools (по умолчанию)** в DevTools используется один и тот же ярлык `F8` .</span><span class="sxs-lookup"><span data-stu-id="5535d-147">With the **DevTools (Default)** preset, the same shortcut in the DevTools is `F8`.</span></span>  <span data-ttu-id="5535d-148">В стиле **кода Visual Studio** ярлык также можно использовать `F5` .</span><span class="sxs-lookup"><span data-stu-id="5535d-148">With the **Visual Studio Code** preset, the shortcut is also `F5`.</span></span>  

### <span data-ttu-id="5535d-149">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="5535d-149">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="5535d-150">Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="5535d-150">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="5535d-151">Вы можете настроить перекрытия в DevTools параметров.</span><span class="sxs-lookup"><span data-stu-id="5535d-151">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="5535d-153">Функция отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="5535d-153">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="5535d-154">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="5535d-154">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="5535d-155">Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-155">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="5535d-156">Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-156">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="5535d-157">Если вы выберете эксперимент, вы можете перемещать инструменты между верхней и нижней панелями, наведя указатель мыши на вкладку, открыв контекстное меню, а затем выбрав пункты **переместить в начало** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="5535d-157">When you choose the experiment, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="5535d-158">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-158">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="5535d-159">Чтобы отобразить или скрыть нижнюю панель, нажмите кнопку `Escape` .</span><span class="sxs-lookup"><span data-stu-id="5535d-159">To show or hide the bottom panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="5535d-161">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="5535d-161">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="5535d-162">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="5535d-162">Enable webhint</span></span>  

<span data-ttu-id="5535d-163">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для обеспечения специальных возможностей, совместимости, безопасности, производительности, PWAs и других распространенных проблем, возникающих при работе в Интернете.</span><span class="sxs-lookup"><span data-stu-id="5535d-163">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="5535d-164">При [эксперименте с DevTools][WebhintMain] на панели " [вопросы][DevtoolsIssues] " появляется обратная связь с помощью подсказки.</span><span class="sxs-lookup"><span data-stu-id="5535d-164">The [webhint][WebhintMain] experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="5535d-165">Вы можете выбрать проблему, чтобы получить сведения о том, как устранить проблему и список уязвимых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="5535d-165">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="5535d-166">Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-166">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="5535d-168">Обратная связь по этой подсказке на панели " **вопросы** "</span><span class="sxs-lookup"><span data-stu-id="5535d-168">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="5535d-169">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="5535d-169">Enable Network Console</span></span>  

<span data-ttu-id="5535d-170">**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="5535d-170">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="5535d-171">Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.</span><span class="sxs-lookup"><span data-stu-id="5535d-171">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="5535d-172">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-172">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="5535d-173">Чтобы использовать консоль "сеть", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5535d-173">To use the Network Console:</span></span>  

1.  <span data-ttu-id="5535d-174">Открытие области " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="5535d-174">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="5535d-175">Найдите сетевой запрос, который вы хотите изменить и отправить повторно.</span><span class="sxs-lookup"><span data-stu-id="5535d-175">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="5535d-176">Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="5535d-176">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="5535d-177">Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="5535d-177">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="5535d-178">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="5535d-178">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.png" alt-text="Сетевая консоль в консольном ящике" lightbox="./media/network-network-console.png":::
   <span data-ttu-id="5535d-180">**Сетевая консоль** в **консольном** ящике</span><span class="sxs-lookup"><span data-stu-id="5535d-180">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### <span data-ttu-id="5535d-181">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="5535d-181">Enable Source Order Viewer</span></span>  

<span data-ttu-id="5535d-182">**Средство просмотра исходного порядка** — это рабочее название эксперимента для отображения порядка элементов в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="5535d-182">**Source Order Viewer** is the working title of an experiment to display the order of elements in the page source.</span></span>  <span data-ttu-id="5535d-183">Вы можете использовать **средство просмотра заказов исходного кода** для поиска проблем с читаемостью на страницах, так как порядок отображения на экране может отличаться от порядка источника, который в противном случае будет обладать предохранителями для пользователей средства чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="5535d-183">You may use the **Source Order Viewer** experiment to find accessibility issues in your pages since the display order on-screen may differ from the order of the source, which confuses screen reader users.</span></span>  

<span data-ttu-id="5535d-184">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-184">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="5535d-185">Чтобы использовать средство просмотра заказов исходного кода, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5535d-185">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="5535d-186">Откройте область **элементы** .</span><span class="sxs-lookup"><span data-stu-id="5535d-186">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="5535d-187">Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).</span><span class="sxs-lookup"><span data-stu-id="5535d-187">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="5535d-188">В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .</span><span class="sxs-lookup"><span data-stu-id="5535d-188">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="5535d-189">Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="5535d-189">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Средство просмотра исходного порядка на панели "Специальные возможности"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="5535d-191">**Средство просмотра исходного порядка** на панели " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="5535d-191">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="5535d-192">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="5535d-192">Previous experimental features</span></span>  

*   <span data-ttu-id="5535d-193">Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="5535d-193">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="5535d-194">Отзывы о экспериментальных функциях</span><span class="sxs-lookup"><span data-stu-id="5535d-194">Providing feedback on experimental features</span></span>  

<span data-ttu-id="5535d-195">Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="5535d-195">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="5535d-196">Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools</span><span class="sxs-lookup"><span data-stu-id="5535d-196">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="5535d-197">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="5535d-197">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>   

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="5535d-199">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5535d-199">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[VisualstudioCode]: https://code.visualstudio.com "Код Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows | Код Microsoft Visual Studio"  

[WebhintMain]: https://webhint.io "Подсказка" 

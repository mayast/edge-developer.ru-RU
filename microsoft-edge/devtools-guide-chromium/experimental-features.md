---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: 19fd59c5dd9f18a681c69250fdcddb22e2796565
ms.sourcegitcommit: f92bf0b50812b43228990b794611daa2144e431c
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2020
ms.locfileid: "10858056"
---
# <span data-ttu-id="040f8-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="040f8-104">Experimental features</span></span>  

<span data-ttu-id="040f8-105">Вы можете использовать экспериментальные функции, которые все еще находятся на стадии разработки в Microsoft Edge DevTools для тестирования и [предоставления отзывов](#providing-feedback-on-experimental-features) , прежде чем они будут выпущены широко.</span><span class="sxs-lookup"><span data-stu-id="040f8-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="040f8-106">Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.</span><span class="sxs-lookup"><span data-stu-id="040f8-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="040f8-107">Включение экспериментальных функций</span><span class="sxs-lookup"><span data-stu-id="040f8-107">Turn on experimental features</span></span>  

<span data-ttu-id="040f8-108">Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="040f8-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="040f8-109">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="040f8-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="040f8-110">Нажмите клавиши `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="040f8-110">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="040f8-111">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="040f8-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="040f8-112">Открытие области [параметров][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="040f8-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="040f8-113">Нажмите клавишу `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="040f8-113">Press `Shift`+`?`.</span></span>  <span data-ttu-id="040f8-114">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="040f8-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="040f8-115">В левой части области **параметров** выберите раздел **эксперименты** .</span><span class="sxs-lookup"><span data-stu-id="040f8-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="040f8-117">Список экспериментов в параметрах DevTools</span><span class="sxs-lookup"><span data-stu-id="040f8-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="040f8-118">На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажки рядом с функциями, которые нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="040f8-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="040f8-119">Закройте и снова откройте Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="040f8-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="040f8-120">Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="040f8-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="040f8-121">Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="040f8-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="040f8-122">Выделены экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="040f8-122">Highlighted experimental features</span></span>  

<span data-ttu-id="040f8-123">В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="040f8-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="040f8-124">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="040f8-124">Experimental feature</span></span> | <span data-ttu-id="040f8-125">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="040f8-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="040f8-126">Вкладка "Включение настраиваемых сочетаний клавиш"</span><span class="sxs-lookup"><span data-stu-id="040f8-126">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="040f8-127">84 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="040f8-127">84 or later</span></span> |
| [<span data-ttu-id="040f8-128">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="040f8-128">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="040f8-129">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="040f8-129">85 or later</span></span> |  
| [<span data-ttu-id="040f8-130">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="040f8-130">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="040f8-131">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="040f8-131">85 or later</span></span> |  
| [<span data-ttu-id="040f8-132">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="040f8-132">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="040f8-133">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="040f8-133">85 or later</span></span> |  

### <span data-ttu-id="040f8-134">Вкладка "Включение настраиваемых сочетаний клавиш"</span><span class="sxs-lookup"><span data-stu-id="040f8-134">Enable custom keyboard shortcuts settings tab</span></span>

<span data-ttu-id="040f8-135">Содержит новую страницу **сочетаний клавиш** в [параметрах DevTools][DevToolsCustomizeSettings] , которая позволяет использовать соответствующие сочетания [клавиш][DevToolsShortcuts] в коде DevTools и [VS][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="040f8-135">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] that enables matching [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [VS Code][VisualstudioCode].</span></span>  

<span data-ttu-id="040f8-136">После включения этого эксперимента снова откройте [Параметры DevTools][DevToolsCustomizeSettings] , нажав `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="040f8-136">Once you have enabled this experiment, open [DevTools Settings][DevToolsCustomizeSettings] again by pressing `Shift`+`?`.</span></span>  <span data-ttu-id="040f8-137">Перейдите на страницу новые **сочетания клавиш** .</span><span class="sxs-lookup"><span data-stu-id="040f8-137">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="040f8-138">Выберите **DevTools (по умолчанию)** в раскрывающемся списке **искать сочетания клавиш из предварительной настройки** и выберите **код Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="040f8-138">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="040f8-139">Сочетания клавиш в DevTools теперь соответствуют сочетаниям клавиш для эквивалентных действий в коде VS.</span><span class="sxs-lookup"><span data-stu-id="040f8-139">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Сопоставление сочетаний клавиш в DevTools с кодом VS" lightbox="./media/experiments-keyboard-shortcut.png":::
   <span data-ttu-id="040f8-141">Сопоставление сочетаний клавиш в DevTools с кодом VS</span><span class="sxs-lookup"><span data-stu-id="040f8-141">Match keyboard shortcuts in the DevTools to VS Code</span></span>
:::image-end:::  

<span data-ttu-id="040f8-142">Например, в Windows для приостановки или продолжения выполнения сценария в [коде VS][VisualstudioCodeShortcutsKeyboardWindows] используется сочетание клавиш `F5` .</span><span class="sxs-lookup"><span data-stu-id="040f8-142">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [VS Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="040f8-143">В стиле **DevTools (Default)** это же сочетание клавиш в DevTools имеет тот же самый ярлык `F8` , что и в **Visual Studio** , но теперь этот ярлык также доступен `F5` .</span><span class="sxs-lookup"><span data-stu-id="040f8-143">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

### <span data-ttu-id="040f8-144">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="040f8-144">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="040f8-145">Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="040f8-145">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="040f8-146">Вы можете настроить перекрытия в DevTools параметров.</span><span class="sxs-lookup"><span data-stu-id="040f8-146">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="040f8-148">Функция отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="040f8-148">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="040f8-149">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="040f8-149">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="040f8-150">Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="040f8-150">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="040f8-151">Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="040f8-151">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="040f8-152">Если выбрать этот эксперимент, вы можете перемещать инструменты между верхней и нижней панелями, наведя указатель мыши на вкладку, открыв контекстное меню (щелкните правой кнопкой \) и выбрав переместить в **Начало** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="040f8-152">When this experiment is selected, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and selecting **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="040f8-153">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="040f8-153">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="040f8-154">Чтобы отобразить или скрыть нижнюю панель, нажмите `Escape` .</span><span class="sxs-lookup"><span data-stu-id="040f8-154">To show or hide the bottom panel, press `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="040f8-156">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="040f8-156">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="040f8-157">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="040f8-157">Enable webhint</span></span>  

<span data-ttu-id="040f8-158">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для обеспечения специальных возможностей, совместимости, безопасности, производительности, PWAs и других распространенных проблем, возникающих при работе в Интернете.</span><span class="sxs-lookup"><span data-stu-id="040f8-158">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="040f8-159">Этот эксперимент приводит к отклику на DevTools на панели " [вопросы][DevtoolsIssues] ".</span><span class="sxs-lookup"><span data-stu-id="040f8-159">This experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="040f8-160">Вы можете выбрать проблему, чтобы получить сведения о том, как устранить проблему и список уязвимых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="040f8-160">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="040f8-161">Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.</span><span class="sxs-lookup"><span data-stu-id="040f8-161">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="040f8-163">Обратная связь по этой подсказке на панели "вопросы"</span><span class="sxs-lookup"><span data-stu-id="040f8-163">webhint feedback in the Issues panel</span></span>  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## <span data-ttu-id="040f8-164">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="040f8-164">Previous experimental features</span></span>  

*   <span data-ttu-id="040f8-165">Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="040f8-165">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="040f8-166">Отзывы о экспериментальных функциях</span><span class="sxs-lookup"><span data-stu-id="040f8-166">Providing feedback on experimental features</span></span>  

<span data-ttu-id="040f8-167">Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="040f8-167">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="040f8-168">Отправка отзыва с помощью значка обратной связи в DevTools</span><span class="sxs-lookup"><span data-stu-id="040f8-168">Send your feedback using the Feedback icon in the DevTools</span></span>  
*   <span data-ttu-id="040f8-169">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="040f8-169">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Значок обратной связи в Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   <span data-ttu-id="040f8-171">Значок обратной связи в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="040f8-171">Feedback icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows | Код Visual Studio"  

[WebhintMain]: https://webhint.io "Подсказка" 

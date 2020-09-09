---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: c78e9aa5e0b4d808dd67d607a954b185ddcf54e7
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004043"
---
# <span data-ttu-id="3d2b5-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="3d2b5-104">Experimental features</span></span>  

<span data-ttu-id="3d2b5-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые все еще находятся на стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="3d2b5-106">Вы можете протестировать и[отдать отзыв](#providing-feedback-on-experimental-features) , прежде чем каждый компонент будет выпущен.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-106">You may test and p[provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="3d2b5-107">Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="3d2b5-108">Включение экспериментальных функций</span><span class="sxs-lookup"><span data-stu-id="3d2b5-108">Turn on experimental features</span></span>  

<span data-ttu-id="3d2b5-109">Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-109">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="3d2b5-110">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-110">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="3d2b5-111">Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3d2b5-111">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="3d2b5-112">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-112">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="3d2b5-113">Открытие области [параметров][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="3d2b5-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="3d2b5-115">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="3d2b5-116">В левой части области **параметров** выберите раздел **эксперименты** .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="3d2b5-118">Список экспериментов в параметрах DevTools</span><span class="sxs-lookup"><span data-stu-id="3d2b5-118">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3d2b5-119">На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажок рядом с каждым компонентом, который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="3d2b5-120">Закройте и снова откройте Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-120">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="3d2b5-121">Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="3d2b5-122">Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="3d2b5-123">Выделены экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="3d2b5-123">Highlighted experimental features</span></span>  

<span data-ttu-id="3d2b5-124">В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="3d2b5-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3d2b5-125">Experimental feature</span></span> | <span data-ttu-id="3d2b5-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d2b5-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="3d2b5-127">Вкладка "Включение настраиваемых сочетаний клавиш"</span><span class="sxs-lookup"><span data-stu-id="3d2b5-127">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="3d2b5-128">84 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="3d2b5-128">84 or later</span></span> |
| [<span data-ttu-id="3d2b5-129">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="3d2b5-129">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="3d2b5-130">84 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="3d2b5-130">84 or later</span></span> |  
| [<span data-ttu-id="3d2b5-131">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="3d2b5-131">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="3d2b5-132">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="3d2b5-132">85 or later</span></span> |  
| [<span data-ttu-id="3d2b5-133">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="3d2b5-133">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="3d2b5-134">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="3d2b5-134">85 or later</span></span> |  
| [<span data-ttu-id="3d2b5-135">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="3d2b5-135">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="3d2b5-136">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="3d2b5-136">85 or later</span></span> |  
| [<span data-ttu-id="3d2b5-137">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="3d2b5-137">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="3d2b5-138">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="3d2b5-138">85 or later</span></span> |  
| [<span data-ttu-id="3d2b5-139">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="3d2b5-139">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="3d2b5-140">86 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="3d2b5-140">86 or later</span></span> |  

### <span data-ttu-id="3d2b5-141">Вкладка "Включение настраиваемых сочетаний клавиш"</span><span class="sxs-lookup"><span data-stu-id="3d2b5-141">Enable custom keyboard shortcuts settings tab</span></span>  

<span data-ttu-id="3d2b5-142">Предоставляет новую страницу **сочетаний клавиш** в [параметрах DevTools][DevToolsCustomizeSettings] для сопоставления [сочетаний клавиш][DevToolsShortcuts] в [коде DevTools с Microsoft Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-142">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] to match [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  

<span data-ttu-id="3d2b5-143">После включения эксперимента снова откройте [Параметры DevTools][DevToolsCustomizeSettings] , нажав кнопку "выбрать" `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-143">After you enable the experiment, open [DevTools Settings][DevToolsCustomizeSettings] again using select `Shift`+`?`.</span></span>  <span data-ttu-id="3d2b5-144">Перейдите на страницу новые **сочетания клавиш** .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-144">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="3d2b5-145">Выберите **DevTools (по умолчанию)** в раскрывающемся списке **искать сочетания клавиш из предварительной настройки** и выберите **код Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-145">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="3d2b5-146">Сочетания клавиш в DevTools теперь соответствуют сочетаниям клавиш для эквивалентных действий в коде Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-146">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="./media/experiments-keyboard-shortcut.msft.png":::
   <span data-ttu-id="3d2b5-148">Соответствие сочетаний клавиш в DevTools с кодом Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d2b5-148">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="3d2b5-149">Например, в Windows для приостановки или продолжения выполнения сценария в [Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] используется сочетание клавиш `F5` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-149">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="3d2b5-150">В стиле **DevTools (по умолчанию)** в DevTools используется один и тот же ярлык `F8` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-150">With the **DevTools (Default)** preset, the same shortcut in the DevTools is `F8`.</span></span>  <span data-ttu-id="3d2b5-151">В стиле **кода Visual Studio** ярлык также можно использовать `F5` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-151">With the **Visual Studio Code** preset, the shortcut is also `F5`.</span></span>  

### <span data-ttu-id="3d2b5-152">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="3d2b5-152">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="3d2b5-153">Предоставляет дополнительные функции для эмуляции двух новых двух экранов и устройств складная в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-153">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="3d2b5-154">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="3d2b5-154">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="3d2b5-155">Samsung Galaxy сгиб</span><span class="sxs-lookup"><span data-stu-id="3d2b5-155">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  

<span data-ttu-id="3d2b5-156">Эмулирует устройства и переключаться между следующими элементами.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-156">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="3d2b5-157">режим с одним экраном или сложением</span><span class="sxs-lookup"><span data-stu-id="3d2b5-157">single-screen or folded posture</span></span>  
*   <span data-ttu-id="3d2b5-158">возможность установки на два экрана или несложенный</span><span class="sxs-lookup"><span data-stu-id="3d2b5-158">dual-screen or unfolded posture</span></span>  

<span data-ttu-id="3d2b5-159">Используйте [экспериментальные API](#enable-experimental-apis) для расширения вашего веб-сайта (или приложения) для устройства.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-159">Use the [enable experimental APIs](#enable-experimental-apis) to enhance your website \(or app\) for a device.</span></span>  <span data-ttu-id="3d2b5-160">Вы также можете использовать [запросы мультимедиа CSS и API перечисления сегмента Windows для JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-160">You may also use the [CSS media queries and the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span></span>  

<!-- This image was taken in Chromium Canary since we don't yet have an Edge Canary that has Stan's changes -->  

:::image type="complex" source="./media/experiments-dual-screen-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="./media/experiments-dual-screen-emulation.msft.png":::  
   <span data-ttu-id="3d2b5-162">Эмуляция Surface Duo в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d2b5-162">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="3d2b5-163">Включение экспериментальных API</span><span class="sxs-lookup"><span data-stu-id="3d2b5-163">Enable experimental APIs</span></span>  

<span data-ttu-id="3d2b5-164">Чтобы [включить этот эксперимент](#turn-on-experimental-features) в Microsoft Edge DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-164">To [enable this experiment](#turn-on-experimental-features) in the Microsoft Edge DevTools, complete the following steps.</span></span>  

1.  <span data-ttu-id="3d2b5-165">Перейдите к `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-165">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="3d2b5-166">В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите " **экспериментальные компоненты веб-платформы** ", а затем **Enabled**— " **Отключить** ".</span><span class="sxs-lookup"><span data-stu-id="3d2b5-166">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="3d2b5-167">Перезапустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-167">Restart Microsoft Edge.</span></span>  

<span data-ttu-id="3d2b5-168">Чтобы улучшить веб-сайт или приложение для двухпроцессорных и складнаяных устройств, перейдите на страницу [запросы CSS и API перечисления сегмента Windows для JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-168">To enhance your website or app for dual-screen and foldable devices, navigate to [CSS media queries and the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span></span>

<span data-ttu-id="3d2b5-169">[Включите этот эксперимент](#turn-on-experimental-features) в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-169">[Turn on this experiment](#turn-on-experimental-features) in the Microsoft Edge DevTools.</span></span>  

1.  <span data-ttu-id="3d2b5-170">Откройте новую вкладку в Microsoft EDGE и перейдите к `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-170">Open a new tab in Microsoft Edge and navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="3d2b5-171">В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите **экспериментальные функции веб-платформы**и измените значение **отключено** на **разрешено**.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-171">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose **Experimental Web Platform features**, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="3d2b5-172">Перезапустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-172">Restart Microsoft Edge.</span></span>  

<span data-ttu-id="3d2b5-173">Дополнительные сведения об улучшении веб-сайта (или приложения) для двухпроцессорных и складнаяных устройств можно найти в [запросах CSS Media и API перечисления сегмента Windows для JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-173">For more information about enhancing your website \(or app\) for dual-screen and foldable devices, navigate to [CSS media queries and the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Флажок включения функций экспериментальной веб-платформы" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="3d2b5-175">Флажок включения функций экспериментальной веб-платформы</span><span class="sxs-lookup"><span data-stu-id="3d2b5-175">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3d2b5-176">Если вы используете запросы на поиск [мультимедиа в каскадных таблицах или API-интерфейс перечисления сегмента Windows (JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables] ) для повышения качества сайта или приложения для служб [Surface Duo][SurfaceDevicesDuo], необходимо также включить флажок **экспериментальные возможности веб-платформы** в [приложении Android Microsoft Edge][GooglePlayMicrosoftEdge] на устройстве [Surface Duo][SurfaceDevicesDuo] .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-176">If you are using [CSS media queries or the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>
> 
> <span data-ttu-id="3d2b5-177">Если флажок **"экспериментальные веб-платформа** " включен [в классическом приложении Microsoft][MicrosoftEdge] EDGE и отключен для [приложения Android Microsoft Edge][GooglePlayMicrosoftEdge], поведение вашего веб-сайта или приложения в эмуляторе Lane Duo в классическом приложении Microsoft EDGE не будет совпадать с [приложением Android Microsoft][GooglePlayMicrosoftEdge] EDGE на [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-177">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge will not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="3d2b5-178">Убедитесь в том, что для устройств Android и Desktop Microsoft Edge успешно используются Эмуляторы Surface Duo в классической платформе [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-178">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="3d2b5-179">Тестирование на устройствах складная и на двух экранах</span><span class="sxs-lookup"><span data-stu-id="3d2b5-179">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="3d2b5-180">При эмуляции [Duo Surface][SurfaceDevicesDuo] в Microsoft EDGE на двух экранах, **стык** прорисовывается на своем веб-сайте или в приложении.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-180">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the **seam** is drawn over your website or app.</span></span>  

> [!NOTE]
> <span data-ttu-id="3d2b5-181">**Стык** — это расстояние между двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-181">The **seam** is the space between the two screens.</span></span>  

<span data-ttu-id="3d2b5-182">Симулятор дисплея для вашего веб-сайта \ (или приложения \) является правильным представлением.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-182">The emulated display for your website \(or app\) is a correct representation.</span></span>  <span data-ttu-id="3d2b5-183">Она будет соответствовать экрану [приложения Android Microsoft Edge][GooglePlayMicrosoftEdge] на [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-183">It matches the display in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="3d2b5-184">Обновите содержимое, чтобы оно лучше отображалось на **стыке**.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-184">Update the content to display better along the **seam**.</span></span>  <span data-ttu-id="3d2b5-185">Для получения дополнительных сведений о адаптации веб-сайта к **стыку**(или внешнему приложению) перейдите к разделу [Работа с стыком][DualScreenIntroductionHowWorkSeam] в документации Surface Duo.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-185">For more information about adapting your website \(or app\) to the **seam**, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam] in the Surface Duo documentation.</span></span>  

<span data-ttu-id="3d2b5-186">На [панели инструментов устройства][DevtoolsDeviceModeIndexSimulateMobileViewport] есть дополнительные функции, с помощью которых можно протестировать веб-сайт или приложение в нескольких элементах управления и ориентации.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-186">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="3d2b5-187">**Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите поворот на (повернуть).</span><span class="sxs-lookup"><span data-stu-id="3d2b5-187">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="3d2b5-188">Объедините функцию с **диапазоном** \ ( ![ Span ][ImageSpanIcon] \), чтобы переключаться между одним экраном или сложением, а также с двойным экраном или без сгиба.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-188">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="3d2b5-189">Вместе функции позволяют тестировать ваш веб-сайт или приложение во всех четырех возможностях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-189">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица геоуровней и ориентации для двухпроцессорных и складная устройств" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="3d2b5-191">Матрица геоуровней и ориентации для двухпроцессорных и складная устройств</span><span class="sxs-lookup"><span data-stu-id="3d2b5-191">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="3d2b5-192">Значок " **экспериментальные веб-платформы** " \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) отображает состояние флага " **экспериментальные веб-платформы** ".</span><span class="sxs-lookup"><span data-stu-id="3d2b5-192">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="3d2b5-193">Если пометка включена, значок выделена.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-193">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="3d2b5-194">Если флажок выключен, значок не выделяется.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-194">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="3d2b5-195">Чтобы включить параметр \ (или выключить), выберите значок или перейдите к нему `edge://flags` и переключите флажок.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-195">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

#### <span data-ttu-id="3d2b5-196">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d2b5-196">Additional resources</span></span>  
*   <span data-ttu-id="3d2b5-197">Дополнительные сведения о разработке можно найти на [веб-сайте с двумя экранами][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-197">For more information about developing, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="3d2b5-198">Установите эмулятор Surface Duo.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-198">Install the Surface Duo emulator].</span></span>  <span data-ttu-id="3d2b5-199">Он отличается от эмулятора в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-199">It is different from the emulator in Microsoft Edge.</span></span>  <span data-ttu-id="3d2b5-200">Она эмулирует на устройстве Surface Duo с Android и интегрируется с [Android Studio][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-200">It emulates the Surface Duo running Android and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="3d2b5-201">Дополнительные сведения можно найти в [пакете SDK Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="3d2b5-201">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

### <span data-ttu-id="3d2b5-202">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="3d2b5-202">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="3d2b5-203">Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-203">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="3d2b5-204">Вы можете настроить перекрытия в DevTools параметров.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-204">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="3d2b5-206">Функция отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="3d2b5-206">CSS grid debugging feature</span></span>  
:::image-end:::  

<span data-ttu-id="3d2b5-207">Чтобы просмотреть последние экспериментальные функции, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-207">To preview the latest experimental features, complete the following actions.</span></span>  

1.  <span data-ttu-id="3d2b5-208">В разделе **эксперименты** выберите параметр **включить параметры отладки для новой сетки каскадных стилей (элементы конфигурации, доступные в области Макет в элементах после перезапуска)** .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-208">In the **Experiments** section, choose the **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)** checkbox.</span></span>  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="3d2b5-209">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="3d2b5-209">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="3d2b5-210">Обычно такие инструменты, как **элементы** и **сеть** , могут открываться только в главной панели, расположенной в верхней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-210">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="3d2b5-211">Такие инструменты, как **трехмерные представления** и **проблемы** , которые обычно закрываются на панели **ящика** , которая находится в нижней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-211">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="3d2b5-212">После выбора эксперимента вы можете перемещать инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-212">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="3d2b5-213">Чтобы переместить инструмент, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **переместить в начало** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-213">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="3d2b5-214">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-214">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="3d2b5-215">Чтобы показать или скрыть панель **ящика** , нажмите кнопку `Escape` .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-215">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="3d2b5-217">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="3d2b5-217">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="3d2b5-218">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="3d2b5-218">Enable webhint</span></span>  

<span data-ttu-id="3d2b5-219">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое предоставляет отзыв в реальном времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-219">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="3d2b5-220">Тип обратной связи, предоставляемой функцией " [Подсказка][WebhintMain]".</span><span class="sxs-lookup"><span data-stu-id="3d2b5-220">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="3d2b5-221">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="3d2b5-221">accessibility</span></span>  
*   <span data-ttu-id="3d2b5-222">совместимость с различными браузерами</span><span class="sxs-lookup"><span data-stu-id="3d2b5-222">cross-browser compatibility</span></span>  
*   <span data-ttu-id="3d2b5-223">безопасность"</span><span class="sxs-lookup"><span data-stu-id="3d2b5-223">security</span></span>  
*   <span data-ttu-id="3d2b5-224">эффективности</span><span class="sxs-lookup"><span data-stu-id="3d2b5-224">performance</span></span>  
*   <span data-ttu-id="3d2b5-225">Приложения PWA</span><span class="sxs-lookup"><span data-stu-id="3d2b5-225">PWAs</span></span>  
*   <span data-ttu-id="3d2b5-226">другие распространенные проблемы с веб-разработками</span><span class="sxs-lookup"><span data-stu-id="3d2b5-226">other common web development issues</span></span>  

<span data-ttu-id="3d2b5-227">Эксперименты с этой [подсказкой][WebhintMain] отображаются на панели " [вопросы][DevtoolsIssues] " в виде обратной связи.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-227">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="3d2b5-228">Выберите вопрос для отображения документации решения и списка уязвимых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-228">Select an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="3d2b5-229">Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-229">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="3d2b5-231">Обратная связь по этой подсказке на панели " **вопросы** "</span><span class="sxs-lookup"><span data-stu-id="3d2b5-231">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="3d2b5-232">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="3d2b5-232">Enable Network Console</span></span>  

<span data-ttu-id="3d2b5-233">**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-233">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="3d2b5-234">Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-234">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="3d2b5-235">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-235">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="3d2b5-236">Чтобы использовать **консоль "сеть**", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-236">To use the **Network Console**, use the following steps.</span></span>    

1.  <span data-ttu-id="3d2b5-237">Открытие области " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="3d2b5-237">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="3d2b5-238">Найдите сетевой запрос, который вы хотите изменить и отправить повторно.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-238">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="3d2b5-239">Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="3d2b5-239">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="3d2b5-240">Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-240">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="3d2b5-241">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-241">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Сетевая консоль в консольном ящике" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="3d2b5-243">**Сетевая консоль** в **консольном** ящике</span><span class="sxs-lookup"><span data-stu-id="3d2b5-243">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="3d2b5-244">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="3d2b5-244">Enable Source Order Viewer</span></span>  

<span data-ttu-id="3d2b5-245">**Средство просмотра исходного порядка** — это эксперимент, в котором отображается порядок элементов в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-245">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="3d2b5-246">Порядок отображения на экране может отличаться от порядка источников, который в своюмся случае будет использовать средство чтения с экрана и пользователи клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-246">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="3d2b5-247">Для поиска различий между порядком отображения на экране и порядком расположения источника используйте эксперимент в **средстве просмотра исходного порядка** .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-247">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="3d2b5-248">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-248">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="3d2b5-249">Чтобы использовать средство просмотра заказов исходного кода, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-249">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="3d2b5-250">Откройте область **элементы** .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-250">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="3d2b5-251">Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).</span><span class="sxs-lookup"><span data-stu-id="3d2b5-251">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="3d2b5-252">В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .</span><span class="sxs-lookup"><span data-stu-id="3d2b5-252">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="3d2b5-253">Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-253">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Средство просмотра исходного порядка на панели "Специальные возможности"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="3d2b5-255">**Средство просмотра исходного порядка** на панели " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="3d2b5-255">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="3d2b5-256">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="3d2b5-256">Previous experimental features</span></span>  

*   <span data-ttu-id="3d2b5-257">Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-257">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="3d2b5-258">Отзывы о экспериментальных функциях</span><span class="sxs-lookup"><span data-stu-id="3d2b5-258">Providing feedback on experimental features</span></span>  

<span data-ttu-id="3d2b5-259">Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d2b5-259">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="3d2b5-260">Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools</span><span class="sxs-lookup"><span data-stu-id="3d2b5-260">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="3d2b5-261">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="3d2b5-261">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="3d2b5-263">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3d2b5-263">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Веб-интерфейс на базе двух экранов | Документы Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получение эмулятора Surface Duo | Документы Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с стыками — введение в работу с устройствами с двумя экранами | Документы Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[VisualstudioCode]: https://code.visualstudio.com "Код Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows | Код Microsoft Visual Studio"  

[GitHubMicrosoftedgeMsedgeexplainerFoldables]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Примитивы веб-платформ для Грамотногоных функций на складная устройствах | GitHub"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy, сгиб | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[WebhintMain]: https://webhint.io "Подсказка"  

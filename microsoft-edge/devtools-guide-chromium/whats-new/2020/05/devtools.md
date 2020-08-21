---
title: Новые возможности в DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: aa39e5d7811d4a614e055a8e0479c74278efbefd
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942189"
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

# <span data-ttu-id="4af37-103">Новые возможности в DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="4af37-103">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <span data-ttu-id="4af37-104">Объявления от команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4af37-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="4af37-105">В следующих разделах приведен список извещений, которые вы пропустили от команды разработчиков Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="4af37-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="4af37-106">Ознакомьтесь с их новыми возможностями в DevTools, расширениях кода VS и многом другом.</span><span class="sxs-lookup"><span data-stu-id="4af37-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="4af37-107">Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge][MicrosoftEdgePreviewChannels] и [отслеживайте нас в Твиттере.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="4af37-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="4af37-108">Использование Средств разработки в режиме высокой контрастности Windows</span><span class="sxs-lookup"><span data-stu-id="4af37-108">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="4af37-109">Средства разработчиков Microsoft Edge теперь отображаются в режиме высокой контрастности, если Windows работает в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="4af37-109">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Разработчики Microsoft Edge в режиме высокой контрастности" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="4af37-111">Разработчики Microsoft Edge в режиме высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="4af37-111">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-112">[Следуйте инструкциям в windows, чтобы включить режим высокой контрастности.][MicrosoftSupportWindows10HighContrastMode]</span><span class="sxs-lookup"><span data-stu-id="4af37-112">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="4af37-113">Откройте DevTools в Microsoft Edge, нажав `F12` или `Ctrl` + `Shift` + `I` клавишу.</span><span class="sxs-lookup"><span data-stu-id="4af37-113">Open the DevTools in Microsoft Edge by pressing `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="4af37-114">В режиме высокой контрастности отображаются разработчики.</span><span class="sxs-lookup"><span data-stu-id="4af37-114">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="4af37-115">В настоящее время в Microsoft Edge DevTools поддерживает режим высокой контрастности для Windows, но не в macOS.</span><span class="sxs-lookup"><span data-stu-id="4af37-115">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span> 

<span data-ttu-id="4af37-116">Проблема с chromium [#1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="4af37-116">Chromium issue [#1048378][CR1048378]</span></span>  

### <span data-ttu-id="4af37-117">Соответствие сочетаниям клавиш в разработчиках на VS-код</span><span class="sxs-lookup"><span data-stu-id="4af37-117">Match keyboard shortcuts in the DevTools to VS Code</span></span>  

<span data-ttu-id="4af37-118">От отзывов [и](#getting-in-touch-with-microsoft-edge-devtools-team) [общедоступного средства разработчика Chromium][CRIssuesList]команда разработчиков Microsoft Edge заработал собой, что вы хотите настраивать сочетания клавиш в средствах разработчиков.</span><span class="sxs-lookup"><span data-stu-id="4af37-118">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="4af37-119">В Microsoft Edge 84 теперь можно использовать сочетания клавиш в Разработчиках с [кодом VS-кода VS,][VSCode]который над ее помощью работает только для настройки сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="4af37-119">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [VS Code][VSCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Соответствие сочетаниям клавиш в разработчиках на VS-код" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="4af37-121">Разработчики Microsoft Edge в режиме высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="4af37-121">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-122">Чтобы попробовать эксперимент, откройте параметры DevTools, нажав или `?` щелкнув ![ значок "Параметры DevTools" в правом верхнем углу ][ImageSettingsIcon] средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="4af37-122">To try the experiment, open DevTools Settings by pressing `?` or selecting the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="4af37-123">Перейдите в раздел **"Эксперименты"** и проверьте параметры сочетаний клавиш **(необходимо перезагрузить) на вкладке "Параметры сочетаний клавиш" (потребуется перезагрузить).**</span><span class="sxs-lookup"><span data-stu-id="4af37-123">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="4af37-124">Теперь снова загрузите DevTools, снова откройте параметры и перейдите в раздел **сочетаний клавиш.**</span><span class="sxs-lookup"><span data-stu-id="4af37-124">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="4af37-125">В **раскрывающемся списке ярлыков "Соответствие" выберите** **пункт Visual Studio Код.** **Match shortcuts from preset**</span><span class="sxs-lookup"><span data-stu-id="4af37-125">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="4af37-126">Сочетания клавиш в разработчиках теперь соответствуют сочетаниям клавиш для эквивалентных действий кода VS-кода.</span><span class="sxs-lookup"><span data-stu-id="4af37-126">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

<span data-ttu-id="4af37-127">Например, сочетание клавиш для привязки или продолжения работы сценария в [коде VS относится][VSCodeShortcuts] к клавише CS. `F5`</span><span class="sxs-lookup"><span data-stu-id="4af37-127">For example, the keyboard shortcut for pausing or continuing running a script in [VS Code][VSCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="4af37-128">В **стандартных средствах DevTools (по умолчанию)** это сочетание клавиш в devTools `F8` **является, но с Visual Studio Code,** теперь это сочетание клавиш `F5` и ярлык.</span><span class="sxs-lookup"><span data-stu-id="4af37-128">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="4af37-129">Функция в настоящее время доступна в Microsoft Edge 84 в качестве экспертов, поэтому сообщите нам об этом с [коллегами.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="4af37-129">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="4af37-130">Проблема с [хромом#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="4af37-130">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="4af37-131">Удаленный отладка Surface Duo emulator</span><span class="sxs-lookup"><span data-stu-id="4af37-131">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="4af37-132">Теперь вы можете удаленно отладки веб-контента работать на [экране эмоблемы Surface Duo][DualScreensAndroidEmulator] с полными возможностями [средств разработчиков Microsoft Edge.][DevToolsChromiumGuide]</span><span class="sxs-lookup"><span data-stu-id="4af37-132">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="4af37-133">[Эмулуатор Surface Duo][DualScreensAndroidEmulator]помогают проверить, как ваш веб-контент будет выводиться на новом классе сгибом и сдвиганием экрана.</span><span class="sxs-lookup"><span data-stu-id="4af37-133">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="4af37-134">Эмулятор работает под управлением операционной системы Android и предоставляет [приложение Microsoft Edge для Android.][AndroidEdge]</span><span class="sxs-lookup"><span data-stu-id="4af37-134">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="4af37-135">Загрузите веб-контент в [приложении Microsoft Edge][AndroidEdge] и отладьте его с помощью [разработчиков Microsoft Edge.][DevToolsChromiumGuide]</span><span class="sxs-lookup"><span data-stu-id="4af37-135">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Приложение Microsoft Edge работает на эмулунере" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="4af37-137">Приложение Microsoft Edge на эмутулу</span><span class="sxs-lookup"><span data-stu-id="4af37-137">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-138">На `edge://inspect` странице в экземпляре [Microsoft Edge][DesktopEdge] отображается список открытых вкладок или [PWS,][PwaIndex] которые выполняются на конвейере [Surface Duo.][DualScreensAndroidEmulator] **SurfaceDuoEmulator**</span><span class="sxs-lookup"><span data-stu-id="4af37-138">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="На edge://inspect появится список открытых вкладок в приложении Microsoft Edge, запущенной на эмляторе" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="4af37-140">На `edge://inspect` странице отображается список открытых вкладок в приложении Microsoft Edge, запущенном на эмляторе</span><span class="sxs-lookup"><span data-stu-id="4af37-140">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="4af37-141">Если выбрать **поиск вкладки или** PWA, которые нужно отладить, [откроется microsoft Edge DevTools.][DevToolsChromiumGuide]</span><span class="sxs-lookup"><span data-stu-id="4af37-141">Selecting **inspect** for the tab or PWA that you want to debug opens the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="4af37-142">Следуйте пошаговым инструкциям, чтобы удаленно отладить [веб-контент на эмоблуровsurface.][DevToolsRemoteDebugDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="4af37-142">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <span data-ttu-id="4af37-143">Удобнее изменить размер рисования DevTools</span><span class="sxs-lookup"><span data-stu-id="4af37-143">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="4af37-144">В Microsoft Edge 83 и более ранних версиях можно изменить размер только средства [рисования DevTools,][DevToolsDrawer] наводя указатель мыши на панель инструментов "Рисование".</span><span class="sxs-lookup"><span data-stu-id="4af37-144">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the Drawer's toolbar.</span></span>  <span data-ttu-id="4af37-145">Рисование отличается от других элементов управления для областей в разработчиках, если наведите указатель мыши на границу области, чтобы изменить ее размер.</span><span class="sxs-lookup"><span data-stu-id="4af37-145">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover over the border of the pane to resize it.</span></span>  <span data-ttu-id="4af37-146">Щелкните на следующем рисунке изображение, чтобы узнать, как изменение рисования, работавшего в версии 83 или более ранних версиях Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4af37-146">Select the following image to see how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Изменение размера средства рисования DevTools в Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="4af37-148">Изменение размера средства рисования DevTools в Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="4af37-148">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="4af37-149">Начиная с Microsoft Edge 84, теперь можно изменить размер рисования, наводя указатель мыши на границу документа.</span><span class="sxs-lookup"><span data-stu-id="4af37-149">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="4af37-150">Это изменение отражает поведение размера других областей средств разработчика с помощью средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="4af37-150">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="4af37-151">Щелкните изображение ниже, чтобы увидеть изменения размера в действии в Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="4af37-151">Select the following image to see resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Изменение размера средствризов DevTools в Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="4af37-153">Изменение размера средствризов DevTools в Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="4af37-153">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="4af37-154">Проблема с chromium [#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="4af37-154">Chromium issue [#1076112][CR1076112]</span></span>  

### <span data-ttu-id="4af37-155">Кнопки навигации экрана с фокусом на кнопках навигации</span><span class="sxs-lookup"><span data-stu-id="4af37-155">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="4af37-156">При удаленном отключении [устройства с Android,][DevToolsRemoteDebugAndroid] [устройства с Windows 10][DevToolsRemoteDebugWindows]или [эмблему Surface Duo][DevToolsRemoteDebugDuoEmulator]вы можете выключать экрансткую выключатель с помощью значка "Выключатель экрана" в левом верхнем углу ![ средств ][ImageScreencastingIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="4af37-156">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="4af37-157">Если включена поддержка экрана, вы сможете перемещаться по вкладке в Microsoft Edge на удаленном устройстве из окна Средств DevTools.</span><span class="sxs-lookup"><span data-stu-id="4af37-157">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="4af37-158">В Microsoft Edge 84 эти кнопки навигации теперь доступны и с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="4af37-158">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="При нажатии клавиш SHIFT+TAB на панели url-адреса экрана фокус переместится на кнопку "Обновить"" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="4af37-160">При нажатии url-адреса на панели вызова `Shift` + `Tab` отображается фокус на **кнопке "Обновить"**</span><span class="sxs-lookup"><span data-stu-id="4af37-160">Pressing `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="4af37-161">Проблема с #1081486 chromium [#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="4af37-161">Chromium issue [#1081486][CR1081486]</span></span>  

### <span data-ttu-id="4af37-162">Панель сведений о панели сетей теперь доступна</span><span class="sxs-lookup"><span data-stu-id="4af37-162">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="4af37-163">В области сведений [Details pane][DevToolsNetworkDetails] в Microsoft **Network** Edge 84 фокус перемещается при ее открытии для ресурса в [журнале сети.][DevToolsNetworkLog]</span><span class="sxs-lookup"><span data-stu-id="4af37-163">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** panel now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="4af37-164">Это изменение позволяет средствам чтения с экрана читать содержимое области **сведений** и работать с ним.</span><span class="sxs-lookup"><span data-stu-id="4af37-164">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="В области сведений в панели "Сетевая сеть" фокус перемещается при открытии" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="4af37-166">В **области сведений в** **панели "Сетевая** сеть" фокус перемещается при открытии</span><span class="sxs-lookup"><span data-stu-id="4af37-166">The **Details** pane in the **Network** panel takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="4af37-167">Проблема с [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="4af37-167">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="4af37-168">Извещения из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="4af37-168">Announcements from the Chromium project</span></span>  

<span data-ttu-id="4af37-169">В следующих разделах описаны дополнительные функции, доступные в Microsoft Edge 84, которые были внесены в проект Chromium.</span><span class="sxs-lookup"><span data-stu-id="4af37-169">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="4af37-170">Устранение проблем с новым средством "Проблемы" в средстве рисования DevTools</span><span class="sxs-lookup"><span data-stu-id="4af37-170">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="4af37-171">Новый **инструмент "Проблемы"** в средстве рисования DevTools встроен для уменьшения количества уведомлений и ненужных элементов **консоли.**</span><span class="sxs-lookup"><span data-stu-id="4af37-171">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="4af37-172">В **настоящее** время консоль — это централизованное место для разработчиков веб-сайтов, библиотек, структур и Microsoft Edge для регистрации сообщений, предупреждений и ошибок.</span><span class="sxs-lookup"><span data-stu-id="4af37-172">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="4af37-173">**Средство** "Проблемы" влияет на предупреждения в браузере в структурированном, обобщаемом и поледо конкретном средстве, ссылки на влияние на ресурсы, на которые влияют на ресурсы в microsoft Edge DevTools, и предоставляет рекомендации по их устранению.</span><span class="sxs-lookup"><span data-stu-id="4af37-173">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="4af37-174">Со временем в средстве "Проблемы" в центре проблем важно появляться больше предупреждений в секторе Microsoft Edge, а не **консоли,** что помогает сократить беспорядок в **консоли.** **Issues**</span><span class="sxs-lookup"><span data-stu-id="4af37-174">Over time, you should see more and more warnings in Microsoft Edge surfacing in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="4af37-175">Чтобы приступить к работе, ознакомьтесь с разделом ["Проблемы с инструментом разработчика Microsoft Edge".][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="4af37-175">To get started, see [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Средство "Проблемы" в средстве рисования Разработчиков" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="4af37-177">Средство **"Проблемы"** в средстве рисования Разработчиков</span><span class="sxs-lookup"><span data-stu-id="4af37-177">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-178">Проблема с [#1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="4af37-178">Chromium issue [#1068116][CR1068116]</span></span>  

### <span data-ttu-id="4af37-179">Просмотр сведений о специальных возможностях в подсказке "Режим проверки"</span><span class="sxs-lookup"><span data-stu-id="4af37-179">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="4af37-180">В **подсказке** теперь указывается, есть ли у элемента доступные названия и [роль][WebhintHintsAxeNameRoleValue] и есть [клавиатура.][WebhintHintsAxeKeyboard]</span><span class="sxs-lookup"><span data-stu-id="4af37-180">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Подсказка в режиме проверки со сведениями о специальных возможностях" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="4af37-182">**Подсказка в режиме** проверки со сведениями о специальных возможностях</span><span class="sxs-lookup"><span data-stu-id="4af37-182">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-183">Проблема с #1040025 chromium [#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="4af37-183">Chromium issue [#1040025][CR1040025]</span></span>  

### <span data-ttu-id="4af37-184">Обновления панели производительности</span><span class="sxs-lookup"><span data-stu-id="4af37-184">Performance panel updates</span></span>  

#### <span data-ttu-id="4af37-185">Просмотр сведений об итоговом блоке в нижнем колонтитуле</span><span class="sxs-lookup"><span data-stu-id="4af37-185">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="4af37-186">После записи скорости загрузки на панели "Производительность" отображаются сведения о дате блокирования времени \(TBT\) в нижнем колонтитуле. **Performance**</span><span class="sxs-lookup"><span data-stu-id="4af37-186">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="4af37-187">Срок погрузки — это показатель производительности, которая помогает квадратить, сколько времени занимает страница.</span><span class="sxs-lookup"><span data-stu-id="4af37-187">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="4af37-188">Фактически измеряет, как долго страница будет отображаться в размере \(так как отображается на экране\); Но не является полезным, так как JavaScript блокирует основной цепочку и поэтому страница не отвечает пользователю.</span><span class="sxs-lookup"><span data-stu-id="4af37-188">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="4af37-189">TBT является основной метрикой приблизительных задержек первого ввода.</span><span class="sxs-lookup"><span data-stu-id="4af37-189">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="4af37-190">Чтобы получить сведения о блокировке времени, не используйте значок **обновления страницы** для ![ ][ImageRefreshPageIcon] загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="4af37-190">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="4af37-191">Вместо этого выберите **значок записи,** вручную перезагрузите страницу, дождитесь ![ ][ImageRecordIcon] загрузки страницы и остановите запись.</span><span class="sxs-lookup"><span data-stu-id="4af37-191">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="4af37-192">Если вы видите, Microsoft Edge DevTools не получал требуемые сведения из `Total Blocking Time: Unavailable` внутренних данных профиля в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4af37-192">If you see `Total Blocking Time: Unavailable`, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Сведения об общем количестве блокировки в нижнем колонтитуле области производительности" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="4af37-194">Сведения об общем количестве блокировки в нижнем колонтитуле **области производительности**</span><span class="sxs-lookup"><span data-stu-id="4af37-194">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-195">Проблема с [хромом#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="4af37-195">Chromium issue [#1054381][CR1054381]</span></span>  

#### <span data-ttu-id="4af37-196">События макета в новом разделе "Возможности"</span><span class="sxs-lookup"><span data-stu-id="4af37-196">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="4af37-197">Новый раздел "Производительность" панели "Производительность" поможет обнаружить смены макета. **Experience** **Performance**</span><span class="sxs-lookup"><span data-stu-id="4af37-197">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="4af37-198">Совместимость макета Shift \(CLS\) позволяет квалифицировать нежелательные визуальные элементы.</span><span class="sxs-lookup"><span data-stu-id="4af37-198">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="4af37-199">Выберите **событие "Смена** макета" для просмотра сведений о смене макета в **области "Сводка".**</span><span class="sxs-lookup"><span data-stu-id="4af37-199">Select the **Layout Shift** event to see the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="4af37-200">Наведите указатель мыши **на перемещенные поля** и **"Перемещенные" в** поля, чтобы наглядно представить, где произошло смена макета.</span><span class="sxs-lookup"><span data-stu-id="4af37-200">Hover over the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Сведения о смене макета" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="4af37-202">Сведения о смене макета</span><span class="sxs-lookup"><span data-stu-id="4af37-202">The details of a layout shift</span></span>  
:::image-end:::  

### <span data-ttu-id="4af37-203">Более тщательно промежуточные термины в консоли</span><span class="sxs-lookup"><span data-stu-id="4af37-203">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="4af37-204">При ведении журнала консоль неправильно предоставлено `Promise` **Console** `PromiseStatus` `resolved` значение.</span><span class="sxs-lookup"><span data-stu-id="4af37-204">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Пример консоли с использованием старого определения терминов" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="4af37-206">Пример консоли **с** использованием `resolved` старого термина</span><span class="sxs-lookup"><span data-stu-id="4af37-206">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-207">Теперь **в консоли используется** термин `fulfilled` , который выравнивается относительно `Promise` спецификации.</span><span class="sxs-lookup"><span data-stu-id="4af37-207">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="4af37-208">Дополнительные сведения о `Promise` спецификации см. в [разделе "Регионы и сборы" на гитме.](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md)</span><span class="sxs-lookup"><span data-stu-id="4af37-208">For more information about the `Promise` specification, see [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Пример консоли с новым терминами" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="4af37-210">Пример **консоли** с новым `fulfilled` терминами</span><span class="sxs-lookup"><span data-stu-id="4af37-210">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-211">Проблема с [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="4af37-211">V8 issue [#6751][CRV86751]</span></span>  

### <span data-ttu-id="4af37-212">Обновления области стилей</span><span class="sxs-lookup"><span data-stu-id="4af37-212">Styles pane updates</span></span>  

#### <span data-ttu-id="4af37-213">Поддержка восстановления ключевых слов</span><span class="sxs-lookup"><span data-stu-id="4af37-213">Support for the revert keyword</span></span>  

<span data-ttu-id="4af37-214">В интерфейсе автозаполнения области **"Стили"** теперь [обнаружение обратного][MDNRevert] ключевого слова CSS, при котором касается касательно вычисленного значения свойства к предыдущему значению.</span><span class="sxs-lookup"><span data-stu-id="4af37-214">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Отмена значения свойства для отмены" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="4af37-216">Отмена значения свойства для отмены</span><span class="sxs-lookup"><span data-stu-id="4af37-216">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-217">Проблема с [#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="4af37-217">Chromium issue [#1075437][CR1075437]</span></span>  

#### <span data-ttu-id="4af37-218">Предварительный просмотр изображений</span><span class="sxs-lookup"><span data-stu-id="4af37-218">Image previews</span></span>  

<span data-ttu-id="4af37-219">Наведите указатель мыши на `background-image` значение в области **"Стили"** для предварительного просмотра изображения в подсказке.</span><span class="sxs-lookup"><span data-stu-id="4af37-219">Hover over a `background-image` value in the **Styles** pane to see a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="При наведении указателя мыши на значение фонового изображения" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="4af37-221">Наведение указателя на `background-image` значение</span><span class="sxs-lookup"><span data-stu-id="4af37-221">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-222">Проблема с [#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="4af37-222">Chromium issue [#1040019][CR1040019]</span></span>  

#### <span data-ttu-id="4af37-223">В средстве выбора цветов теперь используется функция с разделителями, разделенными между пробелами</span><span class="sxs-lookup"><span data-stu-id="4af37-223">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="4af37-224">[Уровень цветового модуля CSS определяет,][CSSWGDraftsColor4Changes3] что функции цвета `rgb()` (например, должны поддерживать аргументы, разделенные пробелами).</span><span class="sxs-lookup"><span data-stu-id="4af37-224">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="4af37-225">Например, команда `rgb(0, 0, 0)` эквивалентна `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="4af37-225">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="4af37-226">При выборе цветов [Color Picker][DevtoolsCssReferenceColorPicker] с помощью средства выбора цветов или альтернативного цветового представления в области **"Стили",** удерживая `Shift` нажатой клавишу `background-color` CTRL, вы увидите синтаксис аргументов, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="4af37-226">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, you should see the space-separated argument syntax.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Использование аргументов разделителей между пробелами в области "Стили"" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="4af37-228">Использование аргументов разделителей между пробелами в **области "Стили"**</span><span class="sxs-lookup"><span data-stu-id="4af37-228">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="4af37-229">Вы также увидите синтаксис в области **вычисляемого** текста и всплывающую подсказку "Режим проверки". **Inspect Mode**</span><span class="sxs-lookup"><span data-stu-id="4af37-229">You should also see the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="4af37-230">В Microsoft Edge DevTools используется новый синтаксис, так как предстоящие функции CSS, [такие как color()][CSSWGDraftsColor4Property] не поддерживают синтаксис устаревшей запятой.</span><span class="sxs-lookup"><span data-stu-id="4af37-230">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="4af37-231">Синтаксис аргументов с разделителями между пробелами поддерживается в большинстве браузеров.</span><span class="sxs-lookup"><span data-stu-id="4af37-231">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="4af37-232">Дополнительные сведения см. в статье ["Можно ли использовать: функция с разделителями"?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="4af37-232">For more information, see [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="4af37-233">Проблема с [#1072952][CR1072952] хромом</span><span class="sxs-lookup"><span data-stu-id="4af37-233">Chromium issue [#1072952][CR1072952]</span></span>  

### <span data-ttu-id="4af37-234">Устаревшее окно "Свойства" в области "Элементы"</span><span class="sxs-lookup"><span data-stu-id="4af37-234">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="4af37-235">Устаревшая область **"Свойства"** на панели "Элементы" устарела. **Properties**</span><span class="sxs-lookup"><span data-stu-id="4af37-235">The **Properties** pane in the **Elements** panel is deprecated.</span></span>  <span data-ttu-id="4af37-236">Вместо `console.dir($0)` этого **запустите консоль.**</span><span class="sxs-lookup"><span data-stu-id="4af37-236">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Область свойств устаревшей" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="4af37-238">Область свойств **устаревшей**</span><span class="sxs-lookup"><span data-stu-id="4af37-238">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <span data-ttu-id="4af37-239">Ссылок</span><span class="sxs-lookup"><span data-stu-id="4af37-239">References</span></span>  

*   [<span data-ttu-id="4af37-240">console.dir()</span><span class="sxs-lookup"><span data-stu-id="4af37-240">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="4af37-241">0 $</span><span class="sxs-lookup"><span data-stu-id="4af37-241">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <span data-ttu-id="4af37-242">Поддержка сочетаний клавиш приложения в области "Манифест"</span><span class="sxs-lookup"><span data-stu-id="4af37-242">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="4af37-243">Сочетания клавиш для приложений помогают пользователям быстро начинать типичные или рекомендуемые задачи в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="4af37-243">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="4af37-244">Меню сочетаний клавиш приложений отображается только для прогрессиональных [веб-приложений,][PwaIndex] установленных на компьютере или мобильном устройстве пользователя.</span><span class="sxs-lookup"><span data-stu-id="4af37-244">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Сочетания клавиш приложений в области манифеста" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="4af37-246">Сочетания клавиш приложений в **области манифеста**</span><span class="sxs-lookup"><span data-stu-id="4af37-246">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="4af37-247">Скачивание каналов с предварительными версиями Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4af37-247">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="4af37-248">Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4af37-248">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="4af37-249">Каналы с предварительными версиями каналов получают доступ к новейшим функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="4af37-249">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="4af37-250">Совместная работа с помощью команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4af37-250">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Значок "Параметры разработчика""
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "DevTools Togle screencast Screencast"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "Значок "Обновить страницу" в области "Производительность""
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "Значок "Запись" панели "Производительность""

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Майкрософт"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir — Ссылка на консоли API | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Объект "Недавно выбранный элемент или объект JavaScript" — API служебных utilities API | Документы Майкрософт"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цветов с помощью средства выбора цветов — CSS Reference | Документы Майкрософт"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Рисование — настройка | Обзор | Документы Майкрософт"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (на базе Chromium) | Документы Майкрософт"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с вкладкой "Проблемы разработчиков" в Microsoft Edge | Документы Майкрософт"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленным отладкой с Устройствами Android | Документы Майкрософт"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Начало работы с удаленным демоэропорой Surface Duo | Документы Майкрософт"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленным отладкой устройств с Windows 10 | Документы Майкрософт"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Проверьте сведения о ресурсе | Документы Майкрософт"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Действия в сети | Документы Майкрософт"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Майкрософт"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Приложение Microsoft Edge для Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Нотация с разделителями с разделителями — MDN | Можно ли использовать"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки на Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: разрешение настройки сочетаний клавиш и привязок | Ошибки на Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не совместимо с WCAG | Ошибки на Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: удобный предварительный просмотр изображений и фоновых изображений в области стилей| Ошибки на Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: показать в свой элемент базовую информацию Ошибки на Chromium"  
[CR1048378]: https://crbug.com/1048378 "Поддержка пользовательского пользовательского образца для режима высокой контрастности | Ошибки на Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Ошибки на Chromium"  
[CR1068116]: https://crbug.com/1068116 "Панель "Проблемы с отправкой" | Ошибки на Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: средство выбора цветов должен создать современный синтаксис цветов CSS | Ошибки на Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: добавление поддержки для ключевого слова и значения | Ошибки на Chromium"  
[CR1076112]: https://crbug.com/1076112 "Персонализация разработки — изменение размера рисования"  
[CR1081486]: https://crbug.com/1081486 "Фокус не отображается для кнопок навигации в режиме экранной шкала | Ошибки на Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus должен быть заполнено, а не соответствует предложению | В8 ошибок v8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Изменения цветов 3 - Модуль цвета CSS уровень 4 | Редактор черновиков группы CSS working Group"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Фон круговый модуль: "цвет" - CSS уровень цвета CSS | Редактор черновиков группы CSS working Group"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Представляем новый браузер Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Штаты и лицы — думанная и промиутбург | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "отмена | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Совместимость браузера | MDN"  

[VSCode]: https://code.visualstudio.com/ "Visual Studio код"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio сочетания клавиш в программах для Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Ось: клавиатура | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Оси: имя роли " | Значение роли | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Включение и отключение режима высокой контрастности в Windows | Поддержка Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools твиттер"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема: MicrosoftDocs/edge-разработчики"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Нужный веб-час"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="4af37-299">Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]</span><span class="sxs-lookup"><span data-stu-id="4af37-299">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4af37-300">Исходная страница [here](https://developers.google.com/web/updates/2020/05/devtools/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4af37-300">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="4af37-302">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4af37-302">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

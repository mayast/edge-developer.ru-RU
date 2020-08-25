---
title: Новые возможности DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f1b5d147aac1b8b527cc7365f9f91a2a7974863e
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942222"
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

# <span data-ttu-id="15fe7-103">Новые возможности DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="15fe7-103">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="15fe7-104">Согласно обновленному календарному плану Chromium мы настраивая наше расписание для предстоящих выпусков Microsoft EDGE и отменив выпуск Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="15fe7-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="15fe7-105">Дополнительные сведения находятся в записи [блога][WindowsBlogStableRelease] .</span><span class="sxs-lookup"><span data-stu-id="15fe7-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="15fe7-106">Ниже описаны новые возможности, доступные в DevTools в Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="15fe7-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="15fe7-107">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="15fe7-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="15fe7-108">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="15fe7-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="15fe7-109">Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.</span><span class="sxs-lookup"><span data-stu-id="15fe7-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="15fe7-110">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="15fe7-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="15fe7-111">Удаленная отладка Microsoft EDGE на устройствах с Windows 10</span><span class="sxs-lookup"><span data-stu-id="15fe7-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="15fe7-112">Приложение [Remote Tools для Microsoft Edge \ (бета-версия)][RemoteTools] теперь доступно в [магазине Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="15fe7-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="15fe7-113">С помощью этого приложения, которое расширяет [портал устройств Windows][WindowsUwpDebugTestPerfDevicePortal], вы можете подключаться из экземпляра Microsoft EDGE, запущенного на компьютере разработки, на удаленное устройство с Windows 10, просмотреть список конечных объектов \ (все вкладки в Microsoft EDGE и [PWAs][PprgressiveWebAppsChromiumIndex] открыть на устройстве с Windows 10 \) и использовать DevTools на своем компьютере для разработки по отношению к целевому объекту на удаленном устройстве с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="15fe7-113">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="15fe7-115">Рисунок 1: приложение [Remote Tools для Microsoft EDGE (Beta)][RemoteTools] , доступное в [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="15fe7-115">Figure 1:  The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-116">[Ознакомьтесь с руководством по настройке устройства с Windows 10 и компьютера для разработки удаленной отладки][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="15fe7-116">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="15fe7-117">Сообщите нам об удаленной отладке, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="15fe7-117">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <span data-ttu-id="15fe7-118">Новые способы доступа к параметрам</span><span class="sxs-lookup"><span data-stu-id="15fe7-118">New ways to access Settings</span></span>  

<span data-ttu-id="15fe7-119">Существует множество параметров для DevTools, которые можно настроить таким образом, чтобы DevTools внешний вид, оформление и работу.</span><span class="sxs-lookup"><span data-stu-id="15fe7-119">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="15fe7-120">В Microsoft Edge 83 доступ к [параметрам][DevtoolsCustomizeIndexSettings] в DevTools теперь стал более простым.</span><span class="sxs-lookup"><span data-stu-id="15fe7-120">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="15fe7-121">Откройте параметры с помощью значка шестеренки рядом с пунктом оповещения консоли и главное меню.</span><span class="sxs-lookup"><span data-stu-id="15fe7-121">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Значок шестеренки, чтобы открыть параметры в DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="15fe7-123">Рисунок 2: значок шестеренки открывает **Параметры** в DevTools</span><span class="sxs-lookup"><span data-stu-id="15fe7-123">Figure 2:  The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-124">Вы также можете открыть [Параметры][DevtoolsCustomizeIndexSettings] из **главного меню** в разделе **Дополнительные инструменты**.</span><span class="sxs-lookup"><span data-stu-id="15fe7-124">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Главное меню > другие инструменты > параметры" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="15fe7-126">Рисунок 3: **главное меню**  >  **Дополнительные**  >  **Параметры** инструментов</span><span class="sxs-lookup"><span data-stu-id="15fe7-126">Figure 3:  **Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-127">[#1050855][CR1050855] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-127">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="15fe7-128">Новые и улучшенные infobars</span><span class="sxs-lookup"><span data-stu-id="15fe7-128">New and improved infobars</span></span>

<span data-ttu-id="15fe7-129">В DevTools теперь есть улучшенные возможности, которые появятся на панелях уведомлений \ (infobars \) на информационной панели.</span><span class="sxs-lookup"><span data-stu-id="15fe7-129">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="15fe7-130">В Microsoft Edge 83 infobars более удобны для чтения и предоставляют кнопки, чтобы можно было принять нужное действие прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="15fe7-130">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Информационная панель для печати файла minified в Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="15fe7-132">Рисунок 4: информационная панель для печати файла minified в Microsoft Edge версии 83</span><span class="sxs-lookup"><span data-stu-id="15fe7-132">Figure 4:  Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-133">[#1056348][CR1056348] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-133">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="15fe7-134">Навигация в окне выбора цвета с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="15fe7-134">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="15fe7-135">[Палитра цветов][DevtoolsCssReferenceColorPicker] — это графический интерфейс пользователя на [панели «элементы»][DevtoolsCssIndex] для изменения `color` и `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="15fe7-135">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="15fe7-136">В предыдущих версиях Microsoft Edge вы не смогли перемещаться по разделу " **тени** " в [палитре цветов][DevtoolsCssReferenceColorPicker] с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="15fe7-136">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Теперь вы можете использовать клавиатуру для перемещения селектора в разделе "тени" палитры цветов" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="15fe7-138">На рисунке 5 показано, как использовать клавиатуру для перемещения селектора в разделе " **тени** " [палитры цветов][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="15fe7-138">Figure 5:  You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-139">В Microsoft Edge 83 теперь можно использовать клавиатуру для перемещения селектора в разделе **тени** окна выбора цвета.</span><span class="sxs-lookup"><span data-stu-id="15fe7-139">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="15fe7-140">[#963183][CR963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-140">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="15fe7-141">Вкладка "Свойства" теперь заполняется после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="15fe7-141">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="15fe7-142">В Microsoft Edge 81 и более ранних версий **вкладка Свойства** на [панели элементы][DevtoolsCssIndex] была разорвана обновлениями страницы.</span><span class="sxs-lookup"><span data-stu-id="15fe7-142">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="15fe7-143">После обновления страницы на **вкладке Свойства** не заполнятся свойства элемента, выбранного в данный момент.</span><span class="sxs-lookup"><span data-stu-id="15fe7-143">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="В Microsoft Edge 81 и более ранних версий вкладка Свойства была пуста после обновления страницы" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="15fe7-145">Рисунок 6: в Microsoft Edge 81 и более ранних версий **вкладка Свойства** была пуста после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="15fe7-145">Figure 6:  In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-146">В Microsoft Edge 83 теперь вы можете видеть свойства элемента, выбранного в данный момент, после обновления страницы на **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="15fe7-146">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="В Microsoft Edge 83 на вкладке Свойства отображаются свойства элемента, выбранного в данный момент, после обновления страницы." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="15fe7-148">Рис. 7: в Microsoft Edge 83 на **вкладке Свойства** отображаются свойства элемента, выбранного в данный момент, после обновления страницы.</span><span class="sxs-lookup"><span data-stu-id="15fe7-148">Figure 7:  In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-149">[#1050999][CR1050999] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-149">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="15fe7-150">Используйте клавиши со стрелками для прокрутки в инструменте "изменения"</span><span class="sxs-lookup"><span data-stu-id="15fe7-150">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="15fe7-151">**Средство "изменения** " отслеживает все изменения, внесенные в CSS или JavaScript, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="15fe7-151">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="15fe7-152">Вы можете использовать **средство "изменения** ", чтобы быстро просмотреть все изменения и вернуть их в редактор или интегрированную среду разработки.</span><span class="sxs-lookup"><span data-stu-id="15fe7-152">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="15fe7-153">Откройте **инструмент "изменения** ", нажав `Ctrl` + `Shift` + `P` в DevTools, чтобы открыть [меню команд][DevToolsCommandMenuIndex] и ввести текст `changes` .</span><span class="sxs-lookup"><span data-stu-id="15fe7-153">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="15fe7-154">Выберите и запустите команду **Показать изменения** , чтобы открыть **средство "изменения** " в DevToolsном ящике.</span><span class="sxs-lookup"><span data-stu-id="15fe7-154">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="15fe7-155">После внесения изменений в файл minified **инструмент "изменения** " позволяет выполнить горизонтальную прокрутку для просмотра всего кода minified.</span><span class="sxs-lookup"><span data-stu-id="15fe7-155">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="15fe7-156">Начиная с Microsoft Edge 83, теперь можно прокручивать по горизонтали с помощью клавиш со стрелками на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="15fe7-156">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="В Microsoft Edge 83 можно выполнить прокрутку по горизонтали с помощью клавиш со стрелками, чтобы просмотреть код minified в инструменте "изменения"." lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="15fe7-158">Рис. 8: в Microsoft Edge 83 вы можете прокручивать текст по горизонтали с помощью клавиш со стрелками, чтобы просмотреть изменения, внесенные в код minified в **инструменте "изменения** ".</span><span class="sxs-lookup"><span data-stu-id="15fe7-158">Figure 8:  In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-159">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="15fe7-159">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="15fe7-160">[#963183][CR963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-160">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="15fe7-161">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-161">Announcements from the Chromium project</span></span>  

<span data-ttu-id="15fe7-162">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 83, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="15fe7-162">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="15fe7-163">Эмуляция видения deficiencies</span><span class="sxs-lookup"><span data-stu-id="15fe7-163">Emulate vision deficiencies</span></span>  

<span data-ttu-id="15fe7-164">Откройте [вкладку рендеринг][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] и воспользуйтесь новой функцией **эмуляции deficiencies** , чтобы лучше понять, как люди с разными типами концепций deficienciesют свой сайт.</span><span class="sxs-lookup"><span data-stu-id="15fe7-164">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Имитация размытого видения" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="15fe7-166">Рисунок 9: Имитация размытого видения</span><span class="sxs-lookup"><span data-stu-id="15fe7-166">Figure 9:  Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-167">DevTools может эмулировать размытое видение и следующие [типы концепций цветопередачи deficiencies][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="15fe7-167">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="15fe7-168">Некоторая концепция цвета</span><span class="sxs-lookup"><span data-stu-id="15fe7-168">Color Vision Deficiency</span></span> | <span data-ttu-id="15fe7-169">Сведения</span><span class="sxs-lookup"><span data-stu-id="15fe7-169">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="15fe7-170">Protanopia</span><span class="sxs-lookup"><span data-stu-id="15fe7-170">Protanopia</span></span> | <span data-ttu-id="15fe7-171">Невозможность воспринимать красный индикатор.</span><span class="sxs-lookup"><span data-stu-id="15fe7-171">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="15fe7-172">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="15fe7-172">Deuteranopia</span></span> | <span data-ttu-id="15fe7-173">Невозможность воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="15fe7-173">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="15fe7-174">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="15fe7-174">Tritanopia</span></span> | <span data-ttu-id="15fe7-175">Невозможность воспринимать любой синий индикатор.</span><span class="sxs-lookup"><span data-stu-id="15fe7-175">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="15fe7-176">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="15fe7-176">Achromatopsia</span></span> | <span data-ttu-id="15fe7-177">Невозможность воспринимать любой цвет, за исключением оттенков серого \ (очень редких).</span><span class="sxs-lookup"><span data-stu-id="15fe7-177">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="15fe7-178">Ниже указаны менее экстремальные версии deficiencies, и в действительности они являются более распространенными.</span><span class="sxs-lookup"><span data-stu-id="15fe7-178">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="15fe7-179">Например, Protanomaly — это уменьшенная чувствительность к красному свету (в отличие от Protanopia, что является полноценным невозможностью воспринимать красный свет).</span><span class="sxs-lookup"><span data-stu-id="15fe7-179">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="15fe7-180">Тем не менее, omaly концепция deficiencies не так четко: каждый человек, имеющий такой интерес, отличается от того, кто имеет такой же интерес, и может по-разному видеть различные варианты (которые могут выпустить больше или меньше подходящих цветов).</span><span class="sxs-lookup"><span data-stu-id="15fe7-180">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="15fe7-181">Благодаря разработке для более экстремальных эмуляций в DevTools веб-приложения будут гарантированно доступны людям с protanomaly, Deuteranomaly, Tritanomaly и achromatomaly.</span><span class="sxs-lookup"><span data-stu-id="15fe7-181">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="15fe7-182">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="15fe7-182">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="15fe7-183">[#1003700][CR1003700] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-183">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="15fe7-184">Эмуляция языков</span><span class="sxs-lookup"><span data-stu-id="15fe7-184">Emulate locales</span></span>  

<span data-ttu-id="15fe7-185">Эмуляция региональных стандартов путем задания местоположения в **Sensors**  >  **расположениях**датчиков.</span><span class="sxs-lookup"><span data-stu-id="15fe7-185">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="15fe7-186">[Открыть **меню команд** ][DevToolsCommandMenuIndex] и ввести текст `Sensors` для доступа к вкладке **Sensors (датчики** ).  После выполнения этих действий DevTools изменяет текущий языковой стандарт по умолчанию, влияя на приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="15fe7-186">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="15fe7-187">API, например:</span><span class="sxs-lookup"><span data-stu-id="15fe7-187">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="15fe7-188">Другие API JavaScript, поддерживающие национальные настройки `String.prototype.localeCompare` , такие как и `*.prototype.toLocaleString` , например:</span><span class="sxs-lookup"><span data-stu-id="15fe7-188">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="15fe7-189">API DOM, например `navigator.language` и</span><span class="sxs-lookup"><span data-stu-id="15fe7-189">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="15fe7-190">[`Accept-Language`][MDNAcceptLanguage]Заголовок HTTP-запроса</span><span class="sxs-lookup"><span data-stu-id="15fe7-190">The [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="15fe7-191">Обновляются `navigator.language` и `navigator.languages` не отображаются немедленно, но только после следующей навигации или обновления страницы.</span><span class="sxs-lookup"><span data-stu-id="15fe7-191">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="15fe7-192">Изменения в `Accept-Language` заголовке HTTP отражаются только для последующих запросов.</span><span class="sxs-lookup"><span data-stu-id="15fe7-192">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Эмуляция языкового стандарта" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="15fe7-194">Рисунок 10: Эмуляция языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="15fe7-194">Figure 10:  Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-195">Чтобы попробовать посмотреть демонстрацию, ознакомьтесь с [примером кода, зависящим от языкового стандарта][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="15fe7-195">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="15fe7-196">[#1051822][CR1051822] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-196">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="15fe7-197">Отладка политики встраивания по началу (COEP)</span><span class="sxs-lookup"><span data-stu-id="15fe7-197">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="15fe7-198">На панели Network (сеть) теперь представлена отладочная информация о [политике встраивания][COEP] .</span><span class="sxs-lookup"><span data-stu-id="15fe7-198">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="15fe7-199">Столбец **Status** теперь содержит краткое описание причины блокировки запроса, а также ссылку на просмотр заголовков этого запроса для дальнейшей отладки.</span><span class="sxs-lookup"><span data-stu-id="15fe7-199">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Заблокированные запросы в столбце \* \* Состояние \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="15fe7-201">Рисунок 11: заблокированные запросы в столбце "состояние"</span><span class="sxs-lookup"><span data-stu-id="15fe7-201">Figure 11:  Blocked requests in the Status column</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-202">В разделе **заголовки ответа** вкладки **заголовки** содержатся дополнительные инструкции по устранению проблем.</span><span class="sxs-lookup"><span data-stu-id="15fe7-202">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Другие рекомендации в разделе "заголовки ответа"" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="15fe7-204">Рисунок 12: дополнительные рекомендации в разделе заголовки ответа</span><span class="sxs-lookup"><span data-stu-id="15fe7-204">Figure 12:  More guidance in the Response Headers section</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-205">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="15fe7-205">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="15fe7-206">[#1051466][CR1051466] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-206">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="15fe7-207">Новые значки для точек останова, условных точек останова и logpoints</span><span class="sxs-lookup"><span data-stu-id="15fe7-207">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="15fe7-208">На панели «источники» есть новые значки для точек останова, условных точек останова и logpoints:</span><span class="sxs-lookup"><span data-stu-id="15fe7-208">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="15fe7-209">Точки останова \ (</span><span class="sxs-lookup"><span data-stu-id="15fe7-209">Breakpoints \(</span></span>![Точкой](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="15fe7-211">\) представлены красными кружками.</span><span class="sxs-lookup"><span data-stu-id="15fe7-211">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="15fe7-212">Условные точки останова \ (</span><span class="sxs-lookup"><span data-stu-id="15fe7-212">Conditional Breakpoints \(</span></span>![Условная точка останова](../../media/2020/03/conditional.msft.png)<span data-ttu-id="15fe7-214">\) представлены в виде кружков из половины белых.</span><span class="sxs-lookup"><span data-stu-id="15fe7-214">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="15fe7-215">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="15fe7-215">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="15fe7-217">\) представлены красными кружками с помощью значков консоли.</span><span class="sxs-lookup"><span data-stu-id="15fe7-217">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="15fe7-218">Мотивация для новых значков — сделать пользовательский интерфейс более подродным с помощью других средств отладки графического интерфейса (обычно это цветовые точки останова), чтобы облегчить различение трех функций.</span><span class="sxs-lookup"><span data-stu-id="15fe7-218">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="15fe7-219">[#1041830][CR1041830] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-219">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="15fe7-220">Просмотр сетевых запросов, заданных для определенного пути к файлу cookie</span><span class="sxs-lookup"><span data-stu-id="15fe7-220">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="15fe7-221">С помощью нового `cookie-path` ключевого слова фильтра на панели **Network (сеть** ) можно сосредоточиться на запросах в сети, которые задают определенный [путь к файлу cookie][MDNCookiePath].</span><span class="sxs-lookup"><span data-stu-id="15fe7-221">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="15fe7-222">Изучите [запросы фильтра по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties] , чтобы найти другие ключевые слова, такие как `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="15fe7-222">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="15fe7-223">Закрепить слева от меню команд</span><span class="sxs-lookup"><span data-stu-id="15fe7-223">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="15fe7-224">Откройте [меню команд][DevToolsCommandMenuIndex] и выполните команду, `Dock to left` чтобы переместить DevTools в левой части окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="15fe7-224">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools закреплен в левой части окна просмотра" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="15fe7-226">Рисунок 13: DevTools закреплен в левой части окна просмотра</span><span class="sxs-lookup"><span data-stu-id="15fe7-226">Figure 13:  DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="15fe7-227">Функция " **прикрепить к левому краю** " была доступна после выпуска Microsoft Edge 75, но ранее она была доступна только в [**главном меню**][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="15fe7-227">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [**Main Menu**][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="15fe7-228">Новая функция в Microsoft Edge 83 — теперь вы можете получить доступ к этой функции в меню команд.</span><span class="sxs-lookup"><span data-stu-id="15fe7-228">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="15fe7-229">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="15fe7-229">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="15fe7-230">[#1011679][CR1011679] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-230">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="15fe7-231">Панель "Аудит" теперь является панелью Lighthouse</span><span class="sxs-lookup"><span data-stu-id="15fe7-231">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="15fe7-232">Группа DevTools часто получила отзыв от веб-разработчиков, которые могли бы запустить [Lighthouse][GithubGoogleChromeLighthouse] из DevTools, когда они могли бы не найти панель "Lighthouse", и панель **аудиторий** стала на панели " **Lighthouse** ".</span><span class="sxs-lookup"><span data-stu-id="15fe7-232">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Панель Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="15fe7-234">Рисунок 14: панель Lighthouse</span><span class="sxs-lookup"><span data-stu-id="15fe7-234">Figure 14:  The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="15fe7-235">Панель **Lighthouse** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="15fe7-235">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="15fe7-236">Корпорация Майкрософт не несет ответственности за содержимое этих сайтов и любые данные, которые могут быть собраны, и не может управлять ими.</span><span class="sxs-lookup"><span data-stu-id="15fe7-236">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="15fe7-237">Удаление всех локальных переопределений в папке</span><span class="sxs-lookup"><span data-stu-id="15fe7-237">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="15fe7-238">После настройки **локальных переопределений** вы можете щелкнуть папку правой кнопкой мыши и выбрать команду создать **все переопределение** для удаления всех локальных переопределений в этой папке.</span><span class="sxs-lookup"><span data-stu-id="15fe7-238">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Удаление всех переопределений" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="15fe7-240">Рисунок 15: удаление всех переопределений</span><span class="sxs-lookup"><span data-stu-id="15fe7-240">Figure 15:  Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-241">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="15fe7-241">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="15fe7-242">[#1016501][CR1016501] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-242">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="15fe7-243">Обновленный пользовательский интерфейс длительных задач</span><span class="sxs-lookup"><span data-stu-id="15fe7-243">Updated Long tasks UI</span></span>  

<span data-ttu-id="15fe7-244">**Длинная задача** — это код JavaScript, который занимает много времени, что приводит к закреплениям веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="15fe7-244">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="15fe7-245">На панели производительности вы можете [визуализировать длинные задачи][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] , но в Microsoft Edge 83 пользовательский интерфейс визуализации задач на панели производительности обновлен.</span><span class="sxs-lookup"><span data-stu-id="15fe7-245">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="15fe7-246">Область задач "Долгая задача" теперь окрашена на красный фон с чередованием.</span><span class="sxs-lookup"><span data-stu-id="15fe7-246">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Новый пользовательский интерфейс длительной задачи" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="15fe7-248">Рисунок 16: новый пользовательский интерфейс длительной задачи</span><span class="sxs-lookup"><span data-stu-id="15fe7-248">Figure 16:  The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="15fe7-249">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="15fe7-249">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="15fe7-250">[#1054447][CR1054447] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="15fe7-250">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="15fe7-251">Поддержка маскированных значков в области манифеста</span><span class="sxs-lookup"><span data-stu-id="15fe7-251">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="15fe7-252">В Oreo Android появились адаптивные значки, которые отображают значки приложений в различных моделях устройств.</span><span class="sxs-lookup"><span data-stu-id="15fe7-252">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="15fe7-253">**Маскированные значки** — это новый формат значков, поддерживающий адаптивные значки, которые позволяют убедиться, что на устройствах, поддерживающих стандарт маскированных значков, будет хорошо выглядеть значок [PWA][PprgressiveWebAppsChromiumIndex] .</span><span class="sxs-lookup"><span data-stu-id="15fe7-253">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="15fe7-254">Установите флажок **Показывать только минимальную безопасную область для маскированных значков** в области **манифеста** , чтобы убедиться в том, что маскирующий значок хорошо подходит для устройств с Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="15fe7-254">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Флажок Показать только минимальную безопасную область для маскированных значков" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="15fe7-256">Рисунок 17: флажок **Показать только минимальную безопасную область для маскированных значков**</span><span class="sxs-lookup"><span data-stu-id="15fe7-256">Figure 17:  The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="15fe7-257">Этот компонент запущен в Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="15fe7-257">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="15fe7-258">Обновления, описанные здесь в Microsoft Edge 83, не были освещены в статье [новые возможности DevTools (Microsoft Edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="15fe7-258">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="15fe7-259">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="15fe7-259">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="15fe7-260">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="15fe7-260">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="15fe7-261">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="15fe7-261">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="15fe7-262">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="15fe7-262">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая ошибка — MicrosoftDocs/Edge-разработчик-GitHub"  
[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительной версии Microsoft Edge"  
[TheWebWeWant]: https://webwewant.fyi "Требуемый веб-сайт"  

[WhatsNew81]: ../01/devtools.md "Новые возможности DevTools (Microsoft Edge 81) | Документы Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цвета с помощью средства выбора цвета | Документы Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Изменение положения в главном меню | Документы Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Просмотр основного действия потока | Документы Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг" | Документы Microsoft"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладкой на устройствах с Windows 10 | Документы Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Точки останова по строке кода: как приостановить выполнение кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Общие сведения о портале устройств Windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Удаленные инструменты для Microsoft EDGE (бета-версия)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Обновление в стабильных выпусках канала для Microsoft Edge"

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Типы цветовой жалюзи"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Одобрение и язык"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Пример кода, зависящий от языкового стандарта"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[CR963183]: https://crbug.com/963183 "Ошибка 963183: DevTools не соответствует требованиям WCAG"  
[CR1003700]: https://crbug.com/1003700 "Вопрос 1003700: Добавление поддержки DevTools в целях моделирования недостатков для представления цвета"  
[CR1011679]: https://crbug.com/1011679 "Ошибка 1011679: ввод "закрепить влево" с помощью меню команд"  
[CR1016501]: https://crbug.com/1016501 "Ошибка 1016501: запрос компонента: кнопка для удаления всех локальных переопределений"  
[CR1050999]: https://crbug.com/1050999 "Ошибка 1050999: вкладка "Свойства""  
[CR1051466]: https://crbug.com/1051466 "Ошибка 1051466: поддержка отладки COOP/COEP в DevTools"  
[CR1054447]: https://crbug.com/1054447 "Ошибка 1054447: обновление метрик производительности на временной шкале DevTools"  
[CR1051822]: https://crbug.com/1051822 "Ошибка 1051822: DevTools: Добавление пользовательского интерфейса для эмуляции национальной настройки"
[CR1041830]: https://crbug.com/1041830 "Ошибка 1041830: улучшение цветопередачи для точек останова"
[CR1050855]: https://crbug.com/1050855 "Неполадка 1050855: Просмотр параметров затрудняет обнаружение"
[CR1056348]: https://crbug.com/1056348 "Ошибка 1056348: обновление компонента на информационной панели"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Описание COOP и COEP — политика opener для разных источников"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Объяснение COOP и COEP — политика для внедрения разных источников"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Репозиторий GitHub Lighthouse"  

> [!NOTE]
> <span data-ttu-id="15fe7-303">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="15fe7-303">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="15fe7-304">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/03/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="15fe7-304">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="15fe7-306">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="15fe7-306">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

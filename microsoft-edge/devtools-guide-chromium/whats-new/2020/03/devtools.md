---
title: Новые возможности DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 17dab9120535ae11ea5a5456552d47dbd7f9e236
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684722"
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







# <span data-ttu-id="41e6f-103">Новые возможности DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="41e6f-103">What's New In DevTools (Microsoft Edge 83)</span></span>   

  

<span data-ttu-id="41e6f-104">Согласно обновленному календарному плану Chromium мы настраивая наше расписание для предстоящих выпусков Microsoft EDGE и отменив выпуск Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="41e6f-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="41e6f-105">Дополнительные сведения находятся в записи [блога][WindowsBlogStableRelease] .</span><span class="sxs-lookup"><span data-stu-id="41e6f-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>

<span data-ttu-id="41e6f-106">Ниже описаны новые возможности, доступные в DevTools в Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="41e6f-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>

## <span data-ttu-id="41e6f-107">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="41e6f-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="41e6f-108">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="41e6f-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="41e6f-109">Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.</span><span class="sxs-lookup"><span data-stu-id="41e6f-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="41e6f-110">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="41e6f-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="41e6f-111">Удаленная отладка Microsoft EDGE на устройствах с Windows 10</span><span class="sxs-lookup"><span data-stu-id="41e6f-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="41e6f-112">Приложение [Remote Tools для Microsoft Edge \ (бета-версия)][RemoteTools] теперь доступно в [магазине Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="41e6f-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="41e6f-113">С помощью этого приложения, которое расширяет [портал устройств Windows][WindowsDevicePortal], вы можете подключаться из экземпляра Microsoft EDGE, запущенного на компьютере разработки, на удаленное устройство с Windows 10, просмотреть список конечных объектов \ (все вкладки в Microsoft EDGE и [PWAs][PWADoc] открыть на устройстве с Windows 10 \) и использовать DevTools на своем компьютере для разработки по отношению к целевому объекту на удаленном устройстве с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="41e6f-113">Using this app, which extends the [Windows Device Portal][WindowsDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PWADoc] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

> ##### <span data-ttu-id="41e6f-114">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="41e6f-114">Figure 1</span></span>  
> <span data-ttu-id="41e6f-115">Приложение [Remote Tools для Microsoft EDGE (бета-версия)][RemoteTools] , доступное в [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="41e6f-115">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
> ![Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store][ImageRemoteTools]  

<span data-ttu-id="41e6f-117">[Ознакомьтесь с руководством по настройке устройства с Windows 10 и компьютера для разработки удаленной отладки][RemoteDebuggingWin10].</span><span class="sxs-lookup"><span data-stu-id="41e6f-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][RemoteDebuggingWin10].</span></span>  <span data-ttu-id="41e6f-118">Сообщите нам об удаленной отладке, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок [обратной связи](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="41e6f-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

### <span data-ttu-id="41e6f-119">Новые способы доступа к параметрам</span><span class="sxs-lookup"><span data-stu-id="41e6f-119">New ways to access Settings</span></span> 

<span data-ttu-id="41e6f-120">Существует множество параметров для DevTools, которые можно настроить таким образом, чтобы DevTools внешний вид, оформление и работу.</span><span class="sxs-lookup"><span data-stu-id="41e6f-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="41e6f-121">В Microsoft Edge 83 доступ к [параметрам][OverviewSettings] в DevTools теперь стал более простым.</span><span class="sxs-lookup"><span data-stu-id="41e6f-121">In Microsoft Edge 83, accessing [Settings][OverviewSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="41e6f-122">Откройте параметры с помощью значка шестеренки рядом с пунктом оповещения консоли и главное меню.</span><span class="sxs-lookup"><span data-stu-id="41e6f-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>

> ##### <span data-ttu-id="41e6f-123">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="41e6f-123">Figure 2</span></span> 
> <span data-ttu-id="41e6f-124">С помощью значка шестеренки в DevTools ![ открывается окно Параметры в DevTools][ImageSettingsGearIcon]</span><span class="sxs-lookup"><span data-stu-id="41e6f-124">The gear icon opens Settings in the DevTools ![The gear icon opens Settings in the DevTools][ImageSettingsGearIcon]</span></span>  

<span data-ttu-id="41e6f-125">Вы также можете открыть [Параметры][OverviewSettings] из **главного меню** в разделе **Дополнительные инструменты**.</span><span class="sxs-lookup"><span data-stu-id="41e6f-125">You are also able to open [Settings][OverviewSettings] from the **Main Menu** under **More tools**.</span></span>

> ##### <span data-ttu-id="41e6f-126">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="41e6f-126">Figure 3</span></span> 
> <span data-ttu-id="41e6f-127">Главное меню > меню "другие инструменты > параметры" ![ > дополнительные инструменты > параметры][ImageSettingsMainMenu]</span><span class="sxs-lookup"><span data-stu-id="41e6f-127">Main Menu > More tools > Settings ![Main Menu > More tools > Settings][ImageSettingsMainMenu]</span></span>  

<span data-ttu-id="41e6f-128">[#1050855][crbug1050855] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-128">Chromium issue [#1050855][crbug1050855]</span></span>

### <span data-ttu-id="41e6f-129">Новые и улучшенные infobars</span><span class="sxs-lookup"><span data-stu-id="41e6f-129">New and improved infobars</span></span>

<span data-ttu-id="41e6f-130">В DevTools теперь есть улучшенные возможности, которые появятся на панелях уведомлений \ (infobars \) на информационной панели.</span><span class="sxs-lookup"><span data-stu-id="41e6f-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="41e6f-131">В Microsoft Edge 83 infobars более удобны для чтения и предоставляют кнопки, чтобы можно было принять нужное действие прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="41e6f-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>

> ##### <span data-ttu-id="41e6f-132">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="41e6f-132">Figure 4</span></span>
> <span data-ttu-id="41e6f-133">Информационная панель для печати файла minified на информационной панели Microsoft Edge 83 ![ для печати файла minified в Microsoft edge 83][ImageInfobar]</span><span class="sxs-lookup"><span data-stu-id="41e6f-133">Infobar for pretty-printing a minified file in Microsoft Edge 83 ![Infobar for pretty-printing a minified file in Microsoft Edge 83][ImageInfobar]</span></span>  

<span data-ttu-id="41e6f-134">[#1056348][crbug1056348] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-134">Chromium issue [#1056348][crbug1056348]</span></span>

### <span data-ttu-id="41e6f-135">Навигация в окне выбора цвета с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="41e6f-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="41e6f-136">[Палитра цветов][ColorPicker] — это графический интерфейс пользователя на [панели «элементы»][ElementsDoc] для изменения `color` и `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="41e6f-136">The [Color Picker][ColorPicker] is a GUI in the [Elements panel][ElementsDoc] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="41e6f-137">В предыдущих версиях Microsoft Edge вы не смогли перемещаться по разделу " **тени** " в [палитре цветов][ColorPicker] с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="41e6f-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][ColorPicker] with the keyboard.</span></span>  

> ##### <span data-ttu-id="41e6f-138">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="41e6f-138">Figure 5</span></span>  
> <span data-ttu-id="41e6f-139">Теперь вы можете использовать клавиатуру для перемещения селектора в разделе " **тени** " [палитры цветов][ColorPicker]</span><span class="sxs-lookup"><span data-stu-id="41e6f-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][ColorPicker]</span></span>  
> ![Теперь вы можете использовать клавиатуру для перемещения селектора в разделе "тени" палитры цветов][ImageColorPicker]  

<span data-ttu-id="41e6f-141">В Microsoft Edge 83 теперь можно использовать клавиатуру для перемещения селектора в разделе **тени** окна выбора цвета.</span><span class="sxs-lookup"><span data-stu-id="41e6f-141">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="41e6f-142">[#963183][crbug963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-142">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="41e6f-143">Вкладка "Свойства" теперь заполняется после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="41e6f-143">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="41e6f-144">В Microsoft Edge 81 и более ранних версий **вкладка Свойства** на [панели элементы][ElementsDoc] была разорвана обновлениями страницы.</span><span class="sxs-lookup"><span data-stu-id="41e6f-144">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][ElementsDoc] was broken by page refreshes.</span></span>  <span data-ttu-id="41e6f-145">После обновления страницы на **вкладке Свойства** не заполнятся свойства элемента, выбранного в данный момент.</span><span class="sxs-lookup"><span data-stu-id="41e6f-145">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

> ##### <span data-ttu-id="41e6f-146">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="41e6f-146">Figure 6</span></span>  
> <span data-ttu-id="41e6f-147">В Microsoft Edge 81 и более ранних версий **вкладка Свойства** была пуста после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="41e6f-147">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
> ![В Microsoft Edge 81 и более ранних версий вкладка Свойства была пуста после обновления страницы][ImagePropertiesIn81]  

<span data-ttu-id="41e6f-149">В Microsoft Edge 83 теперь вы можете видеть свойства элемента, выбранного в данный момент, после обновления страницы на **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="41e6f-149">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

> ##### <span data-ttu-id="41e6f-150">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="41e6f-150">Figure 7</span></span>  
> <span data-ttu-id="41e6f-151">В Microsoft Edge 83 на **вкладке Свойства** отображаются свойства элемента, выбранного в данный момент, после обновления страницы.</span><span class="sxs-lookup"><span data-stu-id="41e6f-151">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
> ![В Microsoft Edge 83 на вкладке Свойства отображаются свойства элемента, выбранного в данный момент, после обновления страницы.][ImagePropertiesIn82]  

<span data-ttu-id="41e6f-153">[#1050999][crbug1050999] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-153">Chromium issue [#1050999][crbug1050999]</span></span>  

### <span data-ttu-id="41e6f-154">Используйте клавиши со стрелками для прокрутки в инструменте "изменения"</span><span class="sxs-lookup"><span data-stu-id="41e6f-154">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="41e6f-155">**Средство "изменения** " отслеживает все изменения, внесенные в CSS или JavaScript, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="41e6f-155">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="41e6f-156">Вы можете использовать **средство "изменения** ", чтобы быстро просмотреть все изменения и вернуть их в редактор или интегрированную среду разработки.</span><span class="sxs-lookup"><span data-stu-id="41e6f-156">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="41e6f-157">Откройте **инструмент "изменения** ", нажав `Ctrl` + `Shift` + `P` в DevTools, чтобы открыть [меню команд][DevToolsCommandMenuIndex] и ввести текст `changes` .</span><span class="sxs-lookup"><span data-stu-id="41e6f-157">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="41e6f-158">Выберите и запустите команду **Показать изменения** , чтобы открыть **средство "изменения** " в DevToolsном ящике.</span><span class="sxs-lookup"><span data-stu-id="41e6f-158">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="41e6f-159">После внесения изменений в файл minified **инструмент "изменения** " позволяет выполнить горизонтальную прокрутку для просмотра всего кода minified.</span><span class="sxs-lookup"><span data-stu-id="41e6f-159">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="41e6f-160">Начиная с Microsoft Edge 83, теперь можно прокручивать по горизонтали с помощью клавиш со стрелками на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="41e6f-160">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

> ##### <span data-ttu-id="41e6f-161">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="41e6f-161">Figure 8</span></span>  
> <span data-ttu-id="41e6f-162">В Microsoft Edge 83 вы можете выполнить горизонтальную прокрутку с помощью клавиш со стрелками, чтобы просмотреть изменения, внесенные в код minified в **инструменте "изменения** ".</span><span class="sxs-lookup"><span data-stu-id="41e6f-162">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
> ![В Microsoft Edge 83 можно выполнить прокрутку по горизонтали с помощью клавиш со стрелками, чтобы просмотреть код minified в инструменте "изменения".][ImageChanges]  

<span data-ttu-id="41e6f-164">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="41e6f-164">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="41e6f-165">[#963183][crbug963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-165">Chromium issue [#963183][crbug963183]</span></span>  

## <span data-ttu-id="41e6f-166">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-166">Announcements from the Chromium project</span></span>  

<span data-ttu-id="41e6f-167">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 83, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="41e6f-167">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="41e6f-168">Эмуляция видения deficiencies</span><span class="sxs-lookup"><span data-stu-id="41e6f-168">Emulate vision deficiencies</span></span>   

<span data-ttu-id="41e6f-169">Откройте [вкладку рендеринг][RenderingDoc] и воспользуйтесь новой функцией **эмуляции deficiencies** , чтобы лучше понять, как люди с разными типами концепций deficienciesют свой сайт.</span><span class="sxs-lookup"><span data-stu-id="41e6f-169">Open the [Rendering tab][RenderingDoc] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

> ##### <span data-ttu-id="41e6f-170">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="41e6f-170">Figure 9</span></span>  
> <span data-ttu-id="41e6f-171">Имитация размытого видения</span><span class="sxs-lookup"><span data-stu-id="41e6f-171">Emulating blurred vision</span></span>  
> ![Имитация размытого видения][ImageEmulatingBlurredVision]  

<span data-ttu-id="41e6f-173">DevTools может эмулировать размытое видение и следующие [типы концепций цветопередачи deficiencies][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="41e6f-173">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="41e6f-174">Некоторая концепция цвета</span><span class="sxs-lookup"><span data-stu-id="41e6f-174">Color Vision Deficiency</span></span> | <span data-ttu-id="41e6f-175">Сведения</span><span class="sxs-lookup"><span data-stu-id="41e6f-175">Details</span></span> |  
|:--- |:--- | 
| <span data-ttu-id="41e6f-176">Protanopia</span><span class="sxs-lookup"><span data-stu-id="41e6f-176">Protanopia</span></span> | <span data-ttu-id="41e6f-177">Невозможность воспринимать красный индикатор.</span><span class="sxs-lookup"><span data-stu-id="41e6f-177">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="41e6f-178">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="41e6f-178">Deuteranopia</span></span> | <span data-ttu-id="41e6f-179">Невозможность воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="41e6f-179">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="41e6f-180">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="41e6f-180">Tritanopia</span></span> | <span data-ttu-id="41e6f-181">Невозможность воспринимать любой синий индикатор.</span><span class="sxs-lookup"><span data-stu-id="41e6f-181">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="41e6f-182">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="41e6f-182">Achromatopsia</span></span> | <span data-ttu-id="41e6f-183">Невозможность воспринимать любой цвет, за исключением оттенков серого \ (очень редких).</span><span class="sxs-lookup"><span data-stu-id="41e6f-183">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> | 

<span data-ttu-id="41e6f-184">Ниже указаны менее экстремальные версии deficiencies, и в действительности они являются более распространенными.</span><span class="sxs-lookup"><span data-stu-id="41e6f-184">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>
<span data-ttu-id="41e6f-185">Например, Protanomaly — это уменьшенная чувствительность к красному свету (в отличие от Protanopia, что является полноценным невозможностью воспринимать красный свет).</span><span class="sxs-lookup"><span data-stu-id="41e6f-185">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="41e6f-186">Тем не менее, omaly концепция deficiencies не так четко: каждый человек, имеющий такой интерес, отличается от того, кто имеет такой же интерес, и может по-разному видеть различные варианты (которые могут выпустить больше или меньше подходящих цветов).</span><span class="sxs-lookup"><span data-stu-id="41e6f-186">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>

<span data-ttu-id="41e6f-187">Благодаря разработке для более экстремальных эмуляций в DevTools веб-приложения будут гарантированно доступны людям с protanomaly, Deuteranomaly, Tritanomaly и achromatomaly.</span><span class="sxs-lookup"><span data-stu-id="41e6f-187">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>

<span data-ttu-id="41e6f-188">Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="41e6f-188">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="41e6f-189">[#1003700][crbug1003700] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-189">Chromium issue [#1003700][crbug1003700]</span></span>  

### <span data-ttu-id="41e6f-190">Эмуляция языков</span><span class="sxs-lookup"><span data-stu-id="41e6f-190">Emulate locales</span></span> 

<span data-ttu-id="41e6f-191">Эмуляция региональных стандартов путем задания местоположения в **Sensors**  >  **расположениях**датчиков.</span><span class="sxs-lookup"><span data-stu-id="41e6f-191">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="41e6f-192">[Открыть **меню команд** ][DevToolsCommandMenuIndex] и ввести текст `Sensors` для доступа к вкладке **Sensors (датчики** ). После выполнения этих действий DevTools изменяет текущий языковой стандарт, который влияет на указанные ниже значения.</span><span class="sxs-lookup"><span data-stu-id="41e6f-192">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab. After performing these actions, DevTools modifies the current default locale, affecting the following:</span></span>

- `Intl.*` <span data-ttu-id="41e6f-193">API, например:</span><span class="sxs-lookup"><span data-stu-id="41e6f-193">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`
- <span data-ttu-id="41e6f-194">другие API JavaScript, поддерживающие национальные настройки `String.prototype.localeCompare` , такие как и `*.prototype.toLocaleString` , например:`123_456..toLocaleString()`</span><span class="sxs-lookup"><span data-stu-id="41e6f-194">other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example: `123_456..toLocaleString()`</span></span>
- <span data-ttu-id="41e6f-195">API DOM, например `navigator.language` и</span><span class="sxs-lookup"><span data-stu-id="41e6f-195">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`
- <span data-ttu-id="41e6f-196">[`Accept-Language`][MDNAcceptLanguage]заголовок HTTP-запроса</span><span class="sxs-lookup"><span data-stu-id="41e6f-196">the [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>

> ##### <span data-ttu-id="41e6f-197">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="41e6f-197">Figure 10</span></span>  
> <span data-ttu-id="41e6f-198">Эмуляция языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="41e6f-198">Emulating a locale</span></span>  
> ![Эмуляция языкового стандарта][ImageEmulatingLocales]  

<span data-ttu-id="41e6f-200">Чтобы попробовать посмотреть демонстрацию, ознакомьтесь с [примером кода, зависящим от языкового стандарта][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="41e6f-200">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="41e6f-201">[#1051822][crbug1051822] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-201">Chromium issue [#1051822][crbug1051822]</span></span>

### <span data-ttu-id="41e6f-202">Отладка по основанным на разных источниках параметрам \ (COEP \)</span><span class="sxs-lookup"><span data-stu-id="41e6f-202">Cross-Origin Embedder Policy \(COEP\) debugging</span></span>   

<span data-ttu-id="41e6f-203">На панели Network (сеть) теперь представлена отладочная информация о [политике встраивания][COEP] .</span><span class="sxs-lookup"><span data-stu-id="41e6f-203">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="41e6f-204">Столбец **Status** теперь содержит краткое описание причины блокировки запроса, а также ссылку на просмотр заголовков этого запроса для дальнейшей отладки.</span><span class="sxs-lookup"><span data-stu-id="41e6f-204">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

> ##### <span data-ttu-id="41e6f-205">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="41e6f-205">Figure 11</span></span>  
> <span data-ttu-id="41e6f-206">Заблокированные запросы в столбце " **состояние** "</span><span class="sxs-lookup"><span data-stu-id="41e6f-206">Blocked requests in the **Status** column</span></span>  
> ![Заблокированные запросы в столбце "состояние"][ImageNetworkStatus]  

<span data-ttu-id="41e6f-208">В разделе **заголовки ответа** вкладки **заголовки** содержатся дополнительные инструкции по устранению проблем.</span><span class="sxs-lookup"><span data-stu-id="41e6f-208">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

> ##### <span data-ttu-id="41e6f-209">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="41e6f-209">Figure 12</span></span>  
> <span data-ttu-id="41e6f-210">Другие рекомендации в разделе "заголовки ответа"</span><span class="sxs-lookup"><span data-stu-id="41e6f-210">More guidance in the Response Headers section</span></span>  
> ![Другие рекомендации в разделе "заголовки ответа"][ImageNetworkGuidance]  

<span data-ttu-id="41e6f-212">Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="41e6f-212">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="41e6f-213">[#1051466][crbug1051466] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-213">Chromium issue [#1051466][crbug1051466]</span></span>  

### <span data-ttu-id="41e6f-214">Просмотр сетевых запросов, заданных для определенного пути к файлу cookie</span><span class="sxs-lookup"><span data-stu-id="41e6f-214">View network requests that set a specific cookie path</span></span> 

<span data-ttu-id="41e6f-215">С помощью нового `cookie-path` ключевого слова фильтра на панели **Network (сеть** ) можно сосредоточиться на запросах в сети, которые задают определенный [путь к файлу cookie][MDNCookiePath].</span><span class="sxs-lookup"><span data-stu-id="41e6f-215">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>

<span data-ttu-id="41e6f-216">Изучите [запросы фильтра по свойствам][NetworkProperties] , чтобы найти другие ключевые слова, такие как `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="41e6f-216">Check out [Filter requests by properties][NetworkProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="41e6f-217">**Закрепить слева** от меню команд</span><span class="sxs-lookup"><span data-stu-id="41e6f-217">**Dock to left** from the Command Menu</span></span>   

<span data-ttu-id="41e6f-218">Откройте [меню команд][DevToolsCommandMenuIndex] и выполните команду, `Dock to left` чтобы переместить DevTools в левой части окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="41e6f-218">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

> ##### <span data-ttu-id="41e6f-219">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="41e6f-219">Figure 13</span></span>  
> <span data-ttu-id="41e6f-220">DevTools закреплен в левой части окна просмотра</span><span class="sxs-lookup"><span data-stu-id="41e6f-220">DevTools docked to the left of the viewport</span></span>  
> ![DevTools закреплен в левой части окна просмотра][ImageDockToLeft]  

> [!NOTE]
> <span data-ttu-id="41e6f-222">Функция " **прикрепить к левому краю** " была доступна после выпуска Microsoft Edge 75, но она ранее была доступна только в [**главном меню**][MainMenuDoc].</span><span class="sxs-lookup"><span data-stu-id="41e6f-222">The **Dock to left** feature has been available since Microsoft Edge 75 but it was previously only accessible from the [**Main Menu**][MainMenuDoc].</span></span>  <span data-ttu-id="41e6f-223">Новая функция в Microsoft Edge 83 — теперь вы можете получить доступ к этой функции в меню команд.</span><span class="sxs-lookup"><span data-stu-id="41e6f-223">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="41e6f-224">Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="41e6f-224">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="41e6f-225">[#1011679][crbug1011679] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-225">Chromium issue [#1011679][crbug1011679]</span></span>  

### <span data-ttu-id="41e6f-226">Панель " **Аудит** " теперь является панелью **Lighthouse**</span><span class="sxs-lookup"><span data-stu-id="41e6f-226">The **Audits** panel is now the **Lighthouse** panel</span></span>   

<span data-ttu-id="41e6f-227">Группа DevTools часто получила отзыв от веб-разработчиков, которые могли бы запустить [Lighthouse][GithubGoogleChromeLighthouse] из DevTools, когда они могли бы не найти панель "Lighthouse", и панель **аудиторий** стала на панели " **Lighthouse** ".</span><span class="sxs-lookup"><span data-stu-id="41e6f-227">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

> ##### <span data-ttu-id="41e6f-228">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="41e6f-228">Figure 14</span></span>  
> <span data-ttu-id="41e6f-229">Панель Lighthouse</span><span class="sxs-lookup"><span data-stu-id="41e6f-229">The Lighthouse panel</span></span>  
> ![Панель Lighthouse][ImageLighthouse]  

> [!NOTE]
> <span data-ttu-id="41e6f-231">Панель **Lighthouse** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="41e6f-231">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="41e6f-232">Корпорация Майкрософт не несет ответственности за содержимое этих сайтов и любые данные, которые могут быть собраны, и не может управлять ими.</span><span class="sxs-lookup"><span data-stu-id="41e6f-232">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="41e6f-233">Удаление всех локальных переопределений в папке</span><span class="sxs-lookup"><span data-stu-id="41e6f-233">Delete all Local Overrides in a folder</span></span>   

<span data-ttu-id="41e6f-234">После настройки **локальных переопределений** вы можете щелкнуть папку правой кнопкой мыши и выбрать команду создать **все переопределение** для удаления всех локальных переопределений в этой папке.</span><span class="sxs-lookup"><span data-stu-id="41e6f-234">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

> ##### <span data-ttu-id="41e6f-235">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="41e6f-235">Figure 15</span></span>  
> <span data-ttu-id="41e6f-236">Удаление всех переопределений</span><span class="sxs-lookup"><span data-stu-id="41e6f-236">Delete all overrides</span></span>  
> ![Удаление всех переопределений][ImageDeleteOverrides]  

<span data-ttu-id="41e6f-238">Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="41e6f-238">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="41e6f-239">[#1016501][crbug1016501] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-239">Chromium issue [#1016501][crbug1016501]</span></span>  

### <span data-ttu-id="41e6f-240">Обновленный пользовательский интерфейс длительных задач</span><span class="sxs-lookup"><span data-stu-id="41e6f-240">Updated Long tasks UI</span></span>   

<span data-ttu-id="41e6f-241">**Длинная задача** — это код JavaScript, который занимает много времени, что приводит к закреплениям веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="41e6f-241">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="41e6f-242">На панели производительности вы можете [визуализировать длинные задачи][LongTasksInPerformancePanel] , но в Microsoft Edge 83 пользовательский интерфейс визуализации задач на панели производительности обновлен.</span><span class="sxs-lookup"><span data-stu-id="41e6f-242">You have been able to [visualize Long Tasks in the Performance panel][LongTasksInPerformancePanel] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="41e6f-243">Область задач "Долгая задача" теперь окрашена на красный фон с чередованием.</span><span class="sxs-lookup"><span data-stu-id="41e6f-243">The Long Task portion of a task is now colored with a striped red background.</span></span>  

> ##### <span data-ttu-id="41e6f-244">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="41e6f-244">Figure 16</span></span>  
> <span data-ttu-id="41e6f-245">Новый пользовательский интерфейс длительной задачи</span><span class="sxs-lookup"><span data-stu-id="41e6f-245">The new Long Task UI</span></span>  
> ![Новый пользовательский интерфейс длительной задачи][ImageLongTask]  

<span data-ttu-id="41e6f-247">Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="41e6f-247">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="41e6f-248">[#1054447][crbug1054447] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="41e6f-248">Chromium issue [#1054447][crbug1054447]</span></span>  

### <span data-ttu-id="41e6f-249">Поддержка маскированных значков в области манифеста</span><span class="sxs-lookup"><span data-stu-id="41e6f-249">Maskable icon support in the Manifest pane</span></span>   

<span data-ttu-id="41e6f-250">В Oreo Android появились адаптивные значки, которые отображают значки приложений в различных моделях устройств.</span><span class="sxs-lookup"><span data-stu-id="41e6f-250">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="41e6f-251">**Маскированные значки** — это новый формат значков, поддерживающий адаптивные значки, которые позволяют убедиться, что на устройствах, поддерживающих стандарт маскированных значков, будет хорошо выглядеть значок [PWA][PWADoc] .</span><span class="sxs-lookup"><span data-stu-id="41e6f-251">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PWADoc] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="41e6f-252">Установите флажок **Показывать только минимальную безопасную область для маскированных значков** в области **манифеста** , чтобы убедиться в том, что маскирующий значок хорошо подходит для устройств с Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="41e6f-252">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

> ##### <span data-ttu-id="41e6f-253">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="41e6f-253">Figure 17</span></span>  
> <span data-ttu-id="41e6f-254">Флажок "Показывать только минимальную безопасную область для маскированных значков"</span><span class="sxs-lookup"><span data-stu-id="41e6f-254">The "Show only the minimum safe area for maskable icons" checkbox</span></span>  
> ![Флажок "Показывать только минимальную безопасную область для маскированных значков"][ImageMaskableIcons]  

> [!NOTE]
> <span data-ttu-id="41e6f-256">Этот компонент запущен в Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="41e6f-256">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="41e6f-257">Обновления, описанные здесь в Microsoft Edge 83, не были освещены в статье [новые возможности DevTools (Microsoft Edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="41e6f-257">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="41e6f-258">Отзыв</span><span class="sxs-lookup"><span data-stu-id="41e6f-258">Feedback</span></span>   

  

<span data-ttu-id="41e6f-259">Чтобы обсудить новые возможности и изменения в этой записи, а также другие связанные с DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="41e6f-259">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="41e6f-260">Отправка отзыва с помощью значка **обратной связи** в DevTools</span><span class="sxs-lookup"><span data-stu-id="41e6f-260">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="41e6f-261">Твит на [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="41e6f-261">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="41e6f-262">Отправка предложения в [Вебе][TheWebWeWant]</span><span class="sxs-lookup"><span data-stu-id="41e6f-262">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="41e6f-263">Ошибки файла в этом документе в репозитории " [Edge — разработчик][GitHubMicrosoftDocsEdgeDeveloperNewIssue] "</span><span class="sxs-lookup"><span data-stu-id="41e6f-263">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

> ##### <span data-ttu-id="41e6f-264">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="41e6f-264">Figure 18</span></span>  
> <span data-ttu-id="41e6f-265">Значок **обратной связи** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="41e6f-265">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![Значок \* \* Feedback \* \* в Microsoft Edge DevTools][ImageFeedbackIcon]  

## <span data-ttu-id="41e6f-267">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41e6f-267">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="41e6f-268">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="41e6f-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="41e6f-269">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="41e6f-269">The preview channels give you access to the latest DevTools features.</span></span>  

<!-- <<../../_shared/devtools-feedback.md>>

<<../../_shared/canary.md>>

<<../../_shared/discover.md>> -->

  

<!-- image links -->  

[ImageRemoteTools]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/remote-tools.msft.png "Рисунок 1: Приложение Remote Tools для Microsoft EDGE (Beta), доступное в Microsoft Store"  
[ImageSettingsGearIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings.msft.png "Рисунок 2: значок шестеренки открывает параметры в DevTools"
[ImageSettingsMainMenu]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings2.msft.png "Рисунок 3: главное меню > другие инструменты > параметры"
[ImageInfobar]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/infobar.msft.png "Рисунок 4: информационная панель для печати файла minified в Microsoft Edge 83"
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/color-picker.msft.png "На рисунке 5 показано, как использовать клавиатуру для перемещения селектора в разделе "тени" палитры цветов"  
[ImagePropertiesIn81]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-81.msft.png "Рисунок 6: в Microsoft Edge 81 и более ранних версий вкладка Свойства была пуста после обновления страницы"  
[ImagePropertiesIn82]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-82.msft.png "Рис. 7: в Microsoft Edge 83 на вкладке Свойства отображаются свойства элемента, выбранного в данный момент, после обновления страницы."  
[ImageChanges]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/changes.msft.png "Рис. 8: в Microsoft Edge 83 вы можете прокручивать текст по горизонтали с помощью клавиш со стрелками, чтобы просмотреть minified код в инструменте "изменения"."  
[ImageEmulatingBlurredVision]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/vision.msft.png "Рисунок 9: Имитация размытого видения"  
[ImageEmulatingLocales]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/locale.msft.png "Рисунок 10: Эмуляция языкового стандарта"
[ImageNetworkStatus]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/status.msft.png "Рисунок 11: заблокированные запросы в столбце "состояние""  
[ImageNetworkGuidance]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/guidance.msft.png "Рисунок 12: дополнительные рекомендации в разделе заголовки ответа"  
[ImageDockToLeft]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/dock-to-left.msft.png "Рисунок 13: DevTools закреплен в левой части окна просмотра"  
[ImageLighthouse]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/lighthouse.msft.png "Рисунок 14: панель Lighthouse"  
[ImageDeleteOverrides]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/overrides.msft.png "Рисунок 15: удаление всех переопределений"  
[ImageLongTask]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/long-task.msft.png "Рисунок 16: новый пользовательский интерфейс длительной задачи"  
[ImageMaskableIcons]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/maskable-icons.msft.png "Рисунок 17: флажок Показать только минимальную безопасную область для маскированных значков"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/feedback-icon.msft.png "Рисунок 18: значок обратной связи в Microsoft Edge DevTools"  

[ImageLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/breakpoint.msft.png
[ImageLogpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/logpoint.msft.png

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "Новые возможности DevTools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цвета с помощью палитры цветов"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Изменение положения в главном меню"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Просмотр основного действия потока"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг""  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения для Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладкой устройств с Windows 10"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Точки останова в коде строки"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Общие сведения о портале устройств Windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Удаленные инструменты для Microsoft EDGE (бета-версия)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Обновление в стабильных выпусках канала для Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Типы цветовой жалюзи"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Одобрение и язык"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Пример кода, зависящий от языкового стандарта"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Ошибка 963183: DevTools не соответствует требованиям WCAG"  
[crbug1003700]: https://crbug.com/1003700 "Вопрос 1003700: Добавление поддержки DevTools в целях моделирования недостатков для представления цвета"  
[crbug1011679]: https://crbug.com/1011679 "Ошибка 1011679: ввод "закрепить влево" с помощью меню команд"  
[crbug1016501]: https://crbug.com/1016501 "Ошибка 1016501: запрос компонента: кнопка для удаления всех локальных переопределений"  
[crbug1050999]: https://crbug.com/1050999 "Ошибка 1050999: вкладка "Свойства""  
[crbug1051466]: https://crbug.com/1051466 "Ошибка 1051466: поддержка отладки COOP/COEP в DevTools"  
[crbug1054447]: https://crbug.com/1054447 "Ошибка 1054447: обновление метрик производительности на временной шкале DevTools"  
[crbug1051822]: https://crbug.com/1051822 "Ошибка 1051822: DevTools: Добавление пользовательского интерфейса для эмуляции национальной настройки"
[crbug1041830]: https://crbug.com/1041830 "Ошибка 1041830: улучшение цветопередачи для точек останова"
[crbug1050855]: https://crbug.com/1050855 "Неполадка 1050855: Просмотр параметров затрудняет обнаружение"
[crbug1056348]: https://crbug.com/1056348 "Ошибка 1056348: обновление компонента на информационной панели"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Описание COOP и COEP — политика opener для разных источников"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Объяснение COOP и COEP — политика для внедрения разных источников"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Репозиторий GitHub Lighthouse"  

> [!NOTE]
> <span data-ttu-id="41e6f-324">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="41e6f-324">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="41e6f-325">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/03/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="41e6f-325">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="41e6f-327">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="41e6f-327">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 59e2f67d773102554b96749690fae51da09428a8
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984198"
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







# <span data-ttu-id="6dd8f-103">Справочные материалы по анализу производительности</span><span class="sxs-lookup"><span data-stu-id="6dd8f-103">Performance analysis reference</span></span>   



<span data-ttu-id="6dd8f-104">На этой странице представлен полный справочник по функциям Microsoft Edge DevTools, относящимися к анализу производительности.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="6dd8f-105">Ознакомьтесь [со статьей анализ производительности среды выполнения][DevtoolsEvaluatePerformanceGettingStarted] для учебного руководства по анализу производительности страницы с помощью [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="6dd8f-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="6dd8f-106">Запись производительности</span><span class="sxs-lookup"><span data-stu-id="6dd8f-106">Record performance</span></span>   

### <span data-ttu-id="6dd8f-107">Запись производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="6dd8f-107">Record runtime performance</span></span>   

<span data-ttu-id="6dd8f-108">Записывайте производительность во время выполнения, когда необходимо проанализировать производительность страницы по мере ее выполнения, а не загрузку.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="6dd8f-109">Перейдите на страницу, которую вы хотите проанализировать.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="6dd8f-110">Откройте вкладку **производительность** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="6dd8f-111">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-111">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="6dd8f-113">Record</span><span class="sxs-lookup"><span data-stu-id="6dd8f-113">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="6dd8f-114">Взаимодействие со страницей.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-114">Interact with the page.</span></span>  <span data-ttu-id="6dd8f-115">DevTools записывает все действия страниц, которые выполняются в результате взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-115">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="6dd8f-116">Нажмите кнопку **запись** еще раз или кнопку **остановить** , чтобы остановить запись.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-116">Click **Record** again or click **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="6dd8f-117">Скорость загрузки записей</span><span class="sxs-lookup"><span data-stu-id="6dd8f-117">Record load performance</span></span>   

<span data-ttu-id="6dd8f-118">Запишите производительность загрузки, когда необходимо проанализировать производительность страницы при ее загрузке, а не на выполнение.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-118">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="6dd8f-119">Перейдите на страницу, которую вы хотите проанализировать.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-119">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="6dd8f-120">Откройте панель " **производительность** " DevTools.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-120">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="6dd8f-121">Нажмите кнопку **обновить страницу** \ ( ![ обновить страницу ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-121">Click **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="6dd8f-122">DevTools записывает метрики производительности во время обновления страницы, а затем автоматически останавливает запись спустя пару секунд после завершения загрузки.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-122">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Обновить страницу" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="6dd8f-124">Обновить страницу</span><span class="sxs-lookup"><span data-stu-id="6dd8f-124">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="6dd8f-125">DevTools автоматически масштабирует часть записи, в которой возникло большинство действий.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-125">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Запись загрузки страницы" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="6dd8f-127">Запись загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="6dd8f-127">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-128">Снимки экрана при записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-128">Capture screenshots while recording</span></span>   

<span data-ttu-id="6dd8f-129">Установите флажок **снимки экрана** , чтобы зафиксировать снимок экрана для каждого кадра во время записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-129">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Флажок "снимки экрана"" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="6dd8f-131">Флажок " **снимки экрана** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-131">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-132">Сведения о том, как работать с снимками экрана, можно найти в разделе [Просмотр снимка экрана](#view-a-screenshot) .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-132">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="6dd8f-133">Принудительная сборка мусора во время записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-133">Force garbage collection while recording</span></span>   

<span data-ttu-id="6dd8f-134">Во время записи страницы нажмите **собрать мусор** \ ( ![ сбор мусора ][ImageCollectGarbageIcon] ) для принудительного сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-134">While you are recording a page, click **Collect garbage** \(![Collect garbage][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Сбор мусора" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="6dd8f-136">Сбор мусора</span><span class="sxs-lookup"><span data-stu-id="6dd8f-136">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-137">Показать параметры записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-137">Show recording settings</span></span>   

<span data-ttu-id="6dd8f-138">Нажмите кнопку **захвата параметров** \ ( ![ Параметры захвата ][ImageCaptureSettingsIcon] ), чтобы предоставить доступ к дополнительным параметрам, связанным с тем, как DevTools захватывает записи производительности.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-138">Click **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Раздел "Параметры захвата"" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="6dd8f-140">Раздел " **Параметры захвата** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-140">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-141">Отключение примеров JavaScript</span><span class="sxs-lookup"><span data-stu-id="6dd8f-141">Disable JavaScript samples</span></span>   

<span data-ttu-id="6dd8f-142">По умолчанию **основной** раздел записи содержит подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-142">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="6dd8f-143">Чтобы отключить эти стеки звонков, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-143">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="6dd8f-144">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-144">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6dd8f-145">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-145">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6dd8f-146">Установите флажок **Отключить образцы JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-146">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="6dd8f-147">Запишите страницу.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-147">Take a recording of the page.</span></span>  
    
<span data-ttu-id="6dd8f-148">На следующих двух рисунках показана разница между отключением и включением образцов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-148">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="6dd8f-149">**Основной** раздел записи становится более коротким, так как выборка отключена, так как при этом не будут выпускаться все стеки вызовов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-149">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Пример записи при отключенных примерах JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="6dd8f-151">Пример записи при отключенных примерах JS</span><span class="sxs-lookup"><span data-stu-id="6dd8f-151">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Пример записи при включенных примерах JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="6dd8f-153">Пример записи при включенных примерах JS</span><span class="sxs-lookup"><span data-stu-id="6dd8f-153">An example of a recording when JS samples are enabled</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="6dd8f-154">Регулирование сети во время записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-154">Throttle the network while recording</span></span>   

<span data-ttu-id="6dd8f-155">Чтобы перерегулировать сеть при записи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-155">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="6dd8f-156">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-156">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6dd8f-157">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-157">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6dd8f-158">Настройте **сеть** для нужного уровня регулирования.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-158">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="6dd8f-159">Регулирование ЦП во время записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-159">Throttle the CPU while recording</span></span>   

<span data-ttu-id="6dd8f-160">Чтобы перерегулировать ЦП во время записи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-160">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="6dd8f-161">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-161">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6dd8f-162">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-162">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6dd8f-163">Установите для **ЦП** требуемый уровень регулирования.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-163">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="6dd8f-164">Регулирование производится относительно возможностей компьютера.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-164">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="6dd8f-165">Например, параметр "интервал по **промедлению** " обеспечивает работу ЦП 2 раза ниже обычного.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-165">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="6dd8f-166">DevTools не имитируют процессоры мобильных устройств, так как архитектура мобильных устройств значительно отличается от настольных компьютеров и ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-166">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="6dd8f-167">Включение расширенного инструментария рисования</span><span class="sxs-lookup"><span data-stu-id="6dd8f-167">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="6dd8f-168">Чтобы просмотреть подробные инструменты для рисования, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-168">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="6dd8f-169">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6dd8f-170">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6dd8f-171">Установите флажок **включить дополнительные возможности инструментирования краски (медленно)** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-171">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="6dd8f-172">Сведения о том, как взаимодействовать с данными краски, можно найти в статье [Просмотр слоев](#view-layers-information) и [профилировщика Paint](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-172">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="6dd8f-173">Сохранение записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-173">Save a recording</span></span>   

<span data-ttu-id="6dd8f-174">Чтобы сохранить запись, щелкните ее правой кнопкой мыши и выберите команду **Сохранить профиль**.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-174">To save a recording, right-click and select **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Сохранить профиль" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="6dd8f-176">Сохранить профиль</span><span class="sxs-lookup"><span data-stu-id="6dd8f-176">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="6dd8f-177">Загрузка записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-177">Load a recording</span></span>   

<span data-ttu-id="6dd8f-178">Чтобы загрузить запись, щелкните ее правой кнопкой мыши и выберите команду " **загрузить профиль**".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-178">To load a recording, right-click and select **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Загрузить профиль" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="6dd8f-180">Загрузить профиль</span><span class="sxs-lookup"><span data-stu-id="6dd8f-180">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="6dd8f-181">Удаление предыдущей записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-181">Clear the previous recording</span></span>   

<span data-ttu-id="6dd8f-182">После внесения записи нажмите **Очистить запись** и ( ![ Очистить запись ][ImageClearRecordingIcon] ), чтобы очистить эту запись на панели **производительности** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-182">After making a recording, press **Clear recording** \(![Clear recording][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Очистка записи" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="6dd8f-184">Очистка записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-184">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="6dd8f-185">Анализ записи производительности</span><span class="sxs-lookup"><span data-stu-id="6dd8f-185">Analyze a performance recording</span></span>   

<span data-ttu-id="6dd8f-186">После того как вы [зарегистрируете производительность во время выполнения](#record-runtime-performance) или [скорость загрузки записи](#record-load-performance), на панели **производительности** можно получить большое количество данных для анализа производительности.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-186">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="6dd8f-187">Выбор части записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-187">Select a portion of a recording</span></span>   

<span data-ttu-id="6dd8f-188">Чтобы выделить часть записи, перетащите указатель мыши по левому или правому краю **обзора** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-188">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="6dd8f-189">**Обзор** — это раздел, содержащий диаграммы в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-189">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Перетащите указатель мыши по обзору, чтобы увеличить масштаб" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="6dd8f-191">Перетащите указатель мыши по **обзору** , чтобы увеличить масштаб</span><span class="sxs-lookup"><span data-stu-id="6dd8f-191">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-192">Чтобы выбрать часть с помощью клавиатуры, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-192">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="6dd8f-193">Щелкните фон **основного** раздела или любой раздел рядом с ним, например **взаимодействия**, **сеть**или **графический процессор**.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-193">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="6dd8f-194">Этот рабочий процесс клавиатуры работает только в том случае, если в фокусе находится один из этих разделов.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-194">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="6dd8f-195">С помощью `W` клавиш,, `A` `S` ,, `D` клавиши для увеличения, перемещения влево, уменьшения и перемещения вправо соответственно.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-195">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="6dd8f-196">Чтобы выбрать часть с помощью сенсорной панели, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-196">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="6dd8f-197">Наведите указатель мыши на раздел **Общие сведения** или на раздел **сведения** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-197">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="6dd8f-198">Раздел **Обзор** — это область, содержащая диаграммы в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-198">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="6dd8f-199">Раздел " **сведения** " — это область, содержащая **основной** раздел, раздел " **взаимодействия** " и т. д.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-199">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="6dd8f-200">С помощью двух пальцев проведите пальцем вверх, проведите пальцем влево, чтобы переместить влево, проведите пальцем вниз, чтобы увеличить масштаб, и проведите пальцем вправо, чтобы перейти вправо.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-200">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="6dd8f-201">Для прокрутки длинной Flame диаграммы в **главном** разделе или любом из соседей щелкните и удерживайте клавишу во время перетаскивания вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-201">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="6dd8f-202">Чтобы переместить выделенную часть записи, перетащите левую и правую клавишу.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-202">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="6dd8f-203">Поиск действий</span><span class="sxs-lookup"><span data-stu-id="6dd8f-203">Search activities</span></span>   

<span data-ttu-id="6dd8f-204">Нажмите клавиши `Control` + `F` \ (Windows \) или `Command` + `F` \ (macOS \), чтобы открыть поле поиска в нижней части панели " **производительность** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-204">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Поле поиска" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="6dd8f-206">Поле поиска</span><span class="sxs-lookup"><span data-stu-id="6dd8f-206">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-207">Чтобы перейти к действиям, которые соответствуют запросу, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-207">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="6dd8f-208">Используйте кнопки **назад** ( ![ предыдущее ][ImagePreviousIcon] ) и **Далее** \ ( ![ Далее ][ImageNextIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-208">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="6dd8f-209">Нажмите кнопку, `Shift` + `Enter` чтобы выбрать предыдущую или `Enter` следующую команду.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-209">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="6dd8f-210">Чтобы изменить параметры запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-210">To modify query settings:</span></span>  

*   <span data-ttu-id="6dd8f-211">Нажмите клавишу **с учетом регистра** \ (с ![ учетом регистра ][ImageSearchCaseIcon] ), чтобы сделать запрос чувствительным к регистру.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-211">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="6dd8f-212">Нажмите **регулярные** выражения \ ( ![ Regex ][ImageSearchRegexIcon] \), чтобы использовать регулярное выражение в запросе.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-212">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="6dd8f-213">Чтобы скрыть поле поиска, нажмите кнопку **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-213">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="6dd8f-214">Просмотр основного действия потока</span><span class="sxs-lookup"><span data-stu-id="6dd8f-214">View main thread activity</span></span>   

<span data-ttu-id="6dd8f-215">Используйте **главный** раздел для просмотра действий, которые произошли в основном потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-215">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Основной раздел" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="6dd8f-217">**Основной** раздел</span><span class="sxs-lookup"><span data-stu-id="6dd8f-217">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-218">Щелкните событие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .  DevTools выделеет выбранное событие.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-218">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Дополнительные сведения о функции Anonymous на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="6dd8f-220">Дополнительные сведения о `anonymous` функции на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-220">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-221">DevTools представляет главную активность потока с Flame диаграммой.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-221">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="6dd8f-222">Ось x обозначает запись с течением времени.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-222">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="6dd8f-223">Ось y представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-223">The y-axis represents the call stack.</span></span>  <span data-ttu-id="6dd8f-224">Событие Top приводит к возникновению событий, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-224">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Flame диаграмма" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="6dd8f-226">Flame диаграмма</span><span class="sxs-lookup"><span data-stu-id="6dd8f-226">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-227">На предыдущем рисунке `click` событие вызвало `Function Call` в `activitytabs.js` строке 53.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-227">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="6dd8f-228">Ниже `Function Call` показано, что была вызвана анонимная функция.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-228">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="6dd8f-229">Анонимная функция, вызываемая, которая вызывается `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-229">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="6dd8f-230">DevTools назначает сценарии случайные цвета.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-230">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="6dd8f-231">На предыдущем рисунке вызовы функций из одного сценария окрашены в зеленый цвет.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-231">In the previous figure, function calls from one script are colored light green.</span></span>  <span data-ttu-id="6dd8f-232">Вызов из другого сценария имеет цветный бежевый.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-232">Calls from another script are colored beige.</span></span>  <span data-ttu-id="6dd8f-233">Темным желтым обозначенными действиями в сценариях, а фиолетовые — действия отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-233">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="6dd8f-234">Эти темные желтые и фиолетовые события будут согласованы во всех записях.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-234">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="6dd8f-235">Если вы хотите скрыть подробную flameную диаграмму вызовов JavaScript, просмотрите раздел [Отключение примеров JavaScript](#disable-javascript-samples) .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-235">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="6dd8f-236">При отключенных примерах JS отображаются только события высокого уровня, такие как `Event: click` и на `Function Call` предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-236">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from the previous figure.</span></span>  

### <span data-ttu-id="6dd8f-237">Просмотр действий в таблице</span><span class="sxs-lookup"><span data-stu-id="6dd8f-237">View activities in a table</span></span>   

<span data-ttu-id="6dd8f-238">После записи страницы, чтобы проанализировать действия, не нужно полагаться только на **основной** раздел.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-238">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="6dd8f-239">DevTools также предоставляет три табличных представления для анализа действий.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-239">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="6dd8f-240">Каждое представление предлагает различные варианты действий:</span><span class="sxs-lookup"><span data-stu-id="6dd8f-240">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="6dd8f-241">Если вы хотите просмотреть корневые действия, которые приводят к большинству работ, используйте [вкладку "дерево вызовов"](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-241">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="6dd8f-242">Если вы хотите просмотреть действия, в которых больше всего потратили время, используйте [вкладку снизу вверх](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-242">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="6dd8f-243">Если вы хотите просмотреть действия в том порядке, в котором они были обнаружены во время записи, используйте [вкладку Журнал событий](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-243">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="6dd8f-244">Следующие три раздела относятся к одной и той же демонстрации.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-244">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="6dd8f-245">Запустите демонстрацию самостоятельно на [вкладке "действия" демонстрации][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="6dd8f-245">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="6dd8f-246">Корневые действия</span><span class="sxs-lookup"><span data-stu-id="6dd8f-246">Root activities</span></span>   

<span data-ttu-id="6dd8f-247">Ниже приведено описание концепции **корневых действий** , упомянутой на вкладке " **дерево вызовов** ", вкладке " **снизу вверх** " и в разделе " **журнал событий** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-247">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="6dd8f-248">Корневые действия — это те, которые приводят к тому, что браузер выполняет определенную работу.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-248">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="6dd8f-249">Например, при щелчке страницы браузер запускает `Event` действие в качестве корневого действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-249">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="6dd8f-250">Это `Event` может привести к запуску обработчика и т. д.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-250">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="6dd8f-251">В диаграмме Flame **основного** раздела корневые действия находятся в верхней части диаграммы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-251">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="6dd8f-252">В **дереве вызовов** и на вкладках **журнал событий** корневые действия — это элементы верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-252">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="6dd8f-253">Пример корневых действий вы видите [на вкладке "дерево вызовов"](#the-call-tree-tab) .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-253">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="6dd8f-254">Вкладка "дерево вызовов"</span><span class="sxs-lookup"><span data-stu-id="6dd8f-254">The Call Tree tab</span></span>   

<span data-ttu-id="6dd8f-255">С помощью вкладки " **дерево вызовов** " можно просмотреть, какие [корневые действия](#root-activities) приводят к наибольшему работоспособности.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-255">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="6dd8f-256">На вкладке " **дерево вызовов** " отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-256">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6dd8f-257">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-257">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Вкладка "дерево вызовов"" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="6dd8f-259">Вкладка " **дерево вызовов** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-259">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-260">На приведенном выше рисунке сверху находятся элементы в столбце " **действия** ", `Evaluate Script` а также `Parse HTML` корневые действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-260">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="6dd8f-261">Вложенный объект представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-261">The nesting represents the call stack.</span></span>  <span data-ttu-id="6dd8f-262">Например, на предыдущем рисунке, `Parse HTML` вызвавшем `Evaluate Script` причины `Compile Script` и `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-262">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="6dd8f-263">**Собственное время** — это время, которое прямо затрачено на это действие.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-263">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="6dd8f-264">**Общее время** представляет время, затраченное на выполнение этого мероприятия или любого из дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-264">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="6dd8f-265">Щелкните **собственное время**, **Общее время**или **активность** , чтобы отсортировать таблицу по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-265">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="6dd8f-266">Используйте текстовое поле " **Фильтр** " для фильтрации событий по имени действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-266">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="6dd8f-267">По умолчанию для меню **Группировка** выбрано значение **Нет группировки**.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-267">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="6dd8f-268">Используйте меню **Группировка** для сортировки таблицы действий на основе различных условий.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-268">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="6dd8f-269">Нажмите кнопку **Показать стоп** -таблицу с максимальным ![ объемом \ (Показать стопку с наиболее тяжелых ][ImageShowHeaviestStackIcon] ), чтобы отобразить другую ячейку справа от таблицы " **действия** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-269">Click **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="6dd8f-270">Щелкните действие, чтобы заполнить таблицу с самым **максимальным** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-270">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="6dd8f-271">В таблице наиболее **плотного стека** показано, какие дочерние элементы выбранного действия занимали наибольшее время.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-271">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="6dd8f-272">Вкладка "снизу вверх"</span><span class="sxs-lookup"><span data-stu-id="6dd8f-272">The Bottom-Up tab</span></span>   

<span data-ttu-id="6dd8f-273">С помощью вкладки " **снизу вверх** " можно просмотреть, какие действия немедленно потратили на общее время в агрегате.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-273">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="6dd8f-274">На вкладке " **снизу вверх** " отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-274">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6dd8f-275">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-275">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Вкладка "снизу вверх"" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="6dd8f-277">Вкладка " **снизу вверх** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-277">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-278">В разделе **основной** Flame диаграммы на предыдущем рисунке показано, что почти практически все время затрачено на работу `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-278">In the **Main** section flame chart of the previous figure, see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="6dd8f-279">Верхнее действие на вкладке " **снизу вверх** " на предыдущем рисунке `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-279">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="6dd8f-280">На вкладке " **снизу вверх** " в списке ниже приведены наиболее ресурсоемкие действия `Layout` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-280">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="6dd8f-281">Столбец " **собственное время** " представляет агрегированное время, проведенное непосредственно в этом действии, для всех вхождений.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-281">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="6dd8f-282">Столбец " **Общее время** " представляет объединенное время, затраченное на это действие или любые дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-282">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="6dd8f-283">Вкладка "журнал событий"</span><span class="sxs-lookup"><span data-stu-id="6dd8f-283">The Event Log tab</span></span>   

<span data-ttu-id="6dd8f-284">Используйте вкладку **журнал событий** , чтобы просмотреть действия в том порядке, в котором они были обнаружены во время записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-284">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="6dd8f-285">На вкладке **журнал событий** отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-285">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6dd8f-286">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-286">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Вкладка "журнал событий"" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="6dd8f-288">Вкладка " **журнал событий** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-288">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-289">Столбец " **время начала** " представляет точку, в которой началось действие, относительно начала записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-289">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="6dd8f-290">Например, время начала `175.7 ms` для выделенного элемента на предыдущем рисунке означает, что действие началось 175,7 MS после начала записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-290">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="6dd8f-291">Столбец " **собственное время** " представляет время, затраченное непосредственно на это действие.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-291">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="6dd8f-292">Столбцы « **Общее время** » обозначают время, затраченное непосредственно на это действие или в любой из дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-292">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="6dd8f-293">Щелкните **время начала**, **собственное время**или **Общее время** для сортировки таблицы по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-293">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="6dd8f-294">Используйте текстовое поле **Фильтр** , чтобы отфильтровать действия по имени.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-294">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="6dd8f-295">С помощью меню " **Длительность** " можно отфильтровать все действия, которые заняли менее 1 мс или 15 мс.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-295">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="6dd8f-296">По умолчанию для меню **Duration** задано значение **все**, что означает, что отображаются все действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-296">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="6dd8f-297">Отключите флажки " **Загрузка**", " **Создание сценариев**", " **Подготовка**" и " **раскраска** ", чтобы отфильтровать все действия из этих категорий.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-297">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="6dd8f-298">Просмотр действий GPU</span><span class="sxs-lookup"><span data-stu-id="6dd8f-298">View GPU activity</span></span>   

<span data-ttu-id="6dd8f-299">Просматривайте активность GPU в разделе **GPU** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-299">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Раздел GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="6dd8f-301">Раздел **GPU**</span><span class="sxs-lookup"><span data-stu-id="6dd8f-301">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-302">Просмотр растровых операций</span><span class="sxs-lookup"><span data-stu-id="6dd8f-302">View raster activity</span></span>   

<span data-ttu-id="6dd8f-303">Просматривайте растровые действия в разделе " **растр** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-303">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Разточечный раздел" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="6dd8f-305">**Разточечный** раздел</span><span class="sxs-lookup"><span data-stu-id="6dd8f-305">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-306">Просмотр взаимодействия</span><span class="sxs-lookup"><span data-stu-id="6dd8f-306">View interactions</span></span>   

<span data-ttu-id="6dd8f-307">В разделе " **взаимодействия** " можно найти и проанализировать взаимодействие с пользователями, произошедшие во время записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-307">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Раздел "взаимодействия"" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="6dd8f-309">Раздел " **взаимодействия** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-309">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-310">Красная линия в нижней части взаимодействия представляет время, затраченное на ожидание основного потока.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-310">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="6dd8f-311">Щелкните взаимодействие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-311">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="6dd8f-312">Анализ кадров в секунду (кадр/с)</span><span class="sxs-lookup"><span data-stu-id="6dd8f-312">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="6dd8f-313">DevTools предлагает многочисленные способы анализа кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-313">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="6dd8f-314">Используйте [диаграмму в кадре](#the-fps-chart) , чтобы получить обзор кадров в кадре в течение не более чем на продолжительность записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-314">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="6dd8f-315">С помощью [раздела кадры](#the-frames-section) вы можете узнать, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-315">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="6dd8f-316">Используйте **индикатор кадров между кадрами** для оценки в режиме реального времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-316">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="6dd8f-317">Показать [количество кадров в секунду в режиме реального времени с индикатором кадров](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-317">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="6dd8f-318">Диаграмма кадр/с</span><span class="sxs-lookup"><span data-stu-id="6dd8f-318">The FPS chart</span></span>   

<span data-ttu-id="6dd8f-319">Диаграмма **кадр/** с — это обзор частоты кадров во время записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-319">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="6dd8f-320">Как правило, чем больше зеленая полоса, тем выше частота кадров.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-320">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="6dd8f-321">Красная черта над диаграммой с индикатором **кадров** — это предупреждение о том, что частота кадров отброшена настолько, что она может повредить взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-321">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Диаграмма кадр/с" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="6dd8f-323">Диаграмма **кадр/** с</span><span class="sxs-lookup"><span data-stu-id="6dd8f-323">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="6dd8f-324">Раздел "кадры"</span><span class="sxs-lookup"><span data-stu-id="6dd8f-324">The Frames section</span></span>   

<span data-ttu-id="6dd8f-325">Раздел **кадры** содержит сведения о том, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-325">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="6dd8f-326">Наведите указатель мыши на кадр, чтобы просмотреть всплывающую подсказку с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-326">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Наведение указателя мыши на рамку" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="6dd8f-328">Наведение указателя мыши на рамку</span><span class="sxs-lookup"><span data-stu-id="6dd8f-328">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-329">Щелкните рамку, чтобы просмотреть дополнительные сведения о кадре на вкладке " **Сводка** ".  DevTools выделеет выделенный кадр синим цветом.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-329">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Просмотр кадра на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="6dd8f-331">Просмотр кадра на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-331">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-332">Просмотр сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="6dd8f-332">View network requests</span></span>   

<span data-ttu-id="6dd8f-333">Разверните раздел **сеть** , чтобы просмотреть каскадные сетевые запросы, которые произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-333">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Раздел "сеть"" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="6dd8f-335">Раздел " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-335">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-336">Запросы записываются цветом следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6dd8f-336">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="6dd8f-337">HTML: синий</span><span class="sxs-lookup"><span data-stu-id="6dd8f-337">HTML: Blue</span></span>  
*   <span data-ttu-id="6dd8f-338">CSS: фиолетовый</span><span class="sxs-lookup"><span data-stu-id="6dd8f-338">CSS: Purple</span></span>  
*   <span data-ttu-id="6dd8f-339">JS: желтый</span><span class="sxs-lookup"><span data-stu-id="6dd8f-339">JS: Yellow</span></span>  
*   <span data-ttu-id="6dd8f-340">Изображения: зеленые</span><span class="sxs-lookup"><span data-stu-id="6dd8f-340">Images: Green</span></span>  
    
<span data-ttu-id="6dd8f-341">Щелкните запрос, чтобы просмотреть дополнительные сведения о нем на вкладке " **Сводка** ".  Например, на предыдущем рисунке на вкладке " **Сводка** " отображаются дополнительные сведения о синем запросе, выбранном в разделе " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-341">Click on a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="6dd8f-342">Темно-синий квадрат в верхней левой части запроса означает, что это запрос более высокого приоритета.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-342">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="6dd8f-343">Более светлый квадрат — более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-343">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="6dd8f-344">Например, на предыдущем рисунке синий, выбранный запрос имеет более высокий приоритет, а зеленый — более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-344">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="6dd8f-345">На первой из приведенных ниже рисунков запрос `www.bing.com` будет представлен линией слева, полосой в середине, темной частью и светлой частью и линией справа.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-345">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="6dd8f-346">На втором рисунке показаны соответствующие представления одного и того же запроса на вкладке **время** на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-346">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="6dd8f-347">Ниже показано, как эти два представления соотносятся друг с другом.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-347">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="6dd8f-348">Левая строка — это все, что нужно для `Connection Start` группы событий (включительно).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-348">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="6dd8f-349">Другими словами, это все, что раньше `Request Sent` , исключительно.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-349">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="6dd8f-350">Светлая часть панели — `Request Sent` и `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-350">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="6dd8f-351">Темная часть панели `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-351">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="6dd8f-352">В настоящее время в течение всего времени, затраченного на ожидание основного потока, в правой строке.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-352">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="6dd8f-353">Этот параметр не отображается на вкладке **время** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-353">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Представление строки запроса www.bing.com в виде линейчатой диаграммы" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="6dd8f-355">Представление запроса в виде строки на строке `www.bing.com`</span><span class="sxs-lookup"><span data-stu-id="6dd8f-355">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Раздел "сеть"" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="6dd8f-357">Раздел " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-357">The **Network** section</span></span>  
<span data-ttu-id="6dd8f-358">::: Image-End:::</span><span class="sxs-lookup"><span data-stu-id="6dd8f-358">:      ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="6dd8f-359">Просмотр метрик памяти</span><span class="sxs-lookup"><span data-stu-id="6dd8f-359">View memory metrics</span></span>   

<span data-ttu-id="6dd8f-360">Включите флажок **память** , чтобы просмотреть метрики памяти от последней записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-360">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Флажок "память"" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="6dd8f-362">Флажок " **память** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-362">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-363">DevTools выводит новую диаграмму с **памятью** над вкладкой **Сводка** .  Кроме того, вы также можете создать новую диаграмму под **чистой** диаграммой, называемой **кучей**.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-363">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="6dd8f-364">Диаграмма **кучи** предоставляет те же данные, что и в линии **кучи JS** в диаграмме с **памятью** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-364">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Метрики памяти" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="6dd8f-366">Метрики памяти</span><span class="sxs-lookup"><span data-stu-id="6dd8f-366">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-367">Цветные линии на диаграмме сопоставляются с цветными флажками над диаграммой.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-367">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="6dd8f-368">Отключите флажок, чтобы скрыть эту категорию на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-368">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="6dd8f-369">На диаграмме отображается только область текущей записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-369">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="6dd8f-370">Например, на предыдущем рисунке диаграмма **памяти** показывает использование памяти только вокруг 400 MS, помечая его на 1750 MS.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-370">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="6dd8f-371">Просмотр длительности части записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-371">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="6dd8f-372">При анализе раздела, например " **сеть** " или " **основной**", иногда требуется более точная оценка продолжительности определенных событий.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-372">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="6dd8f-373">`Shift`Чтобы выделить часть записи, перетащите указатель влево или вправо, удерживая нажатой клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-373">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="6dd8f-374">В нижней части выделенного фрагмента DevTools показывает, сколько времени заняло эта часть.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-374">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Просмотр длительности части записи" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="6dd8f-376">Просмотр длительности части записи</span><span class="sxs-lookup"><span data-stu-id="6dd8f-376">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-377">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="6dd8f-377">View a screenshot</span></span>   

<span data-ttu-id="6dd8f-378">Сведения о включении снимков экрана можно найти в разделе [запись снимков экрана](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-378">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="6dd8f-379">Наведите указатель мыши на **Обзор** , чтобы просмотреть снимок экрана, на котором размещается страница в этот момент записи.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-379">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="6dd8f-380">**Обзор** — это раздел, содержащий диаграммы **ЦП**, **кадров между кадрами**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-380">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Просмотр снимка экрана" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="6dd8f-382">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="6dd8f-382">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-383">Вы также можете просмотреть снимки экрана, щелкнув кадр в разделе **кадры** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-383">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="6dd8f-384">DevTools отображает маленькую версию снимка экрана на вкладке " **Сводка** ".</span><span class="sxs-lookup"><span data-stu-id="6dd8f-384">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Просмотр снимка экрана на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="6dd8f-386">Просмотр снимка экрана на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-386">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-387">Щелкните эскиз на вкладке " **Сводка** ", чтобы увеличить масштаб на снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-387">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Изменение масштаба экрана на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="6dd8f-389">Изменение масштаба экрана на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-389">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="6dd8f-390">Просмотр сведений о слоях</span><span class="sxs-lookup"><span data-stu-id="6dd8f-390">View layers information</span></span>   

<span data-ttu-id="6dd8f-391">Чтобы просмотреть дополнительные сведения о кадре, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-391">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="6dd8f-392">[Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-392">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="6dd8f-393">Выберите кадр в разделе **кадры** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-393">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="6dd8f-394">DevTools отображает сведения о слоях на вкладке Создание **слоев** рядом с вкладкой **журнал событий** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-394">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Область слоев" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="6dd8f-396">Область **слоев**</span><span class="sxs-lookup"><span data-stu-id="6dd8f-396">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6dd8f-397">Наведите указатель мыши на слой, чтобы выделить его на схеме.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-397">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Выделение слоя" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="6dd8f-399">Выделение слоя</span><span class="sxs-lookup"><span data-stu-id="6dd8f-399">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="6dd8f-400">Чтобы переместить схему, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-400">To move the diagram:</span></span>  

*   <span data-ttu-id="6dd8f-401">Щелкните **режим панорамирования** \ ( ![ режим панорамирования ][ImagePanModeIcon] ), чтобы перемещаться вдоль осей X и Y.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-401">Click **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="6dd8f-402">Выберите **режим поворота** \ ( ![ режим поворота ][ImageRotateModeIcon] \) для поворота вдоль оси Z.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-402">Click **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="6dd8f-403">Нажмите кнопку **Сброс преобразования** \ ( ![ Сброс преобразования ][ImageResetTransformIcon] ), чтобы восстановить исходное расположение схемы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-403">Click **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="6dd8f-404">Просмотр профилировщика Paint</span><span class="sxs-lookup"><span data-stu-id="6dd8f-404">View paint profiler</span></span>   

<span data-ttu-id="6dd8f-405">Чтобы просмотреть дополнительные сведения о событии Paint, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-405">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="6dd8f-406">[Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-406">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="6dd8f-407">Выберите событие **Paint** в **главном** разделе.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-407">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Вкладка "профилировщик Paint"" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="6dd8f-409">Вкладка " **профилировщик Paint** "</span><span class="sxs-lookup"><span data-stu-id="6dd8f-409">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6dd8f-410">Анализ производительности отрисовки с помощью вкладки "рендеринг"</span><span class="sxs-lookup"><span data-stu-id="6dd8f-410">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="6dd8f-411">С помощью функций вкладки " **отрисовка** " можно визуализировать эффективность отрисовки страницы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-411">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="6dd8f-412">Чтобы открыть вкладку **рендеринга** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-412">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="6dd8f-413">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="6dd8f-413">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="6dd8f-414">Начните вводить текст `Rendering` и выберите его `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-414">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="6dd8f-415">DevTools отображает вкладку **рендеринг** в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-415">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Вкладка «рендеринг»" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="6dd8f-417">Вкладка « **рендеринг** »</span><span class="sxs-lookup"><span data-stu-id="6dd8f-417">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="6dd8f-418">Просмотр кадров в секунду в режиме реального времени с индикатором кадров</span><span class="sxs-lookup"><span data-stu-id="6dd8f-418">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="6dd8f-419">**Индикатор кадров в кадрах** — это наложение, которое отображается в правом верхнем углу окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-419">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="6dd8f-420">Она предоставляет оценку кадров в реальном времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-420">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="6dd8f-421">Чтобы открыть **индикатор кадров**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-421">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="6dd8f-422">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-422">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6dd8f-423">Включите флажок **индикатор кадров в кадре** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-423">Enable the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Индикатор кадров в кадре" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="6dd8f-425">**Индикатор кадров в кадре**</span><span class="sxs-lookup"><span data-stu-id="6dd8f-425">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="6dd8f-426">Просмотр событий рисования в реальном времени с помощью помигания Paint</span><span class="sxs-lookup"><span data-stu-id="6dd8f-426">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="6dd8f-427">Чтобы получить представление о всех событиях рисования на странице в реальном времени, используйте Paint.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-427">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="6dd8f-428">Каждый раз, когда часть страницы зарисуется повторно, DevTools разменяет его зеленым цветом.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-428">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="6dd8f-429">Чтобы включить мигание краски, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="6dd8f-429">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="6dd8f-430">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-430">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6dd8f-431">Установите флажок **закрасить мигающий** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-431">Enable the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Мигание краски" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="6dd8f-433">Мигание краски</span><span class="sxs-lookup"><span data-stu-id="6dd8f-433">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="6dd8f-434">Просмотр наложения слоев с границами слоев</span><span class="sxs-lookup"><span data-stu-id="6dd8f-434">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="6dd8f-435">Используйте **границы слоев** для просмотра наложенных границ слоев и плиток в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-435">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="6dd8f-436">Чтобы включить границы слоев, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-436">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="6dd8f-437">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-437">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6dd8f-438">Установите флажок **границы слоя** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-438">Enable the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Границы слоев" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="6dd8f-440">Границы слоев</span><span class="sxs-lookup"><span data-stu-id="6dd8f-440">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="6dd8f-441">Ознакомьтесь с комментариями [`debug_colors.cc`][ChromiumDebugColors] , изложенными в разделе Описание цветовых кодирования.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-441">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="6dd8f-442">Поиск проблем с производительностью прокрутки в реальном времени</span><span class="sxs-lookup"><span data-stu-id="6dd8f-442">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="6dd8f-443">Используйте проблемы с производительностью прокрутки, чтобы идентифицировать элементы страницы, которые содержат прослушиватели событий, связанные с прокруткой, которые могут повредить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-443">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="6dd8f-444">DevTools поменяет потенциально проблематичные элементы в синем тексте.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-444">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="6dd8f-445">Для просмотра проблем с производительностью прокрутки:</span><span class="sxs-lookup"><span data-stu-id="6dd8f-445">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="6dd8f-446">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-446">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6dd8f-447">Включите флажок **проблемы с прокруткой** .</span><span class="sxs-lookup"><span data-stu-id="6dd8f-447">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Прокрутка проблем с производительностью указывает на то, что объекты просмотра, не связанные с разслойю, могут повредить производительность при прокрутке." lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="6dd8f-449">**Прокрутка проблем с производительностью** указывает на то, что объекты просмотра, не связанные с разслойю, могут повредить производительность при прокрутке.</span><span class="sxs-lookup"><span data-stu-id="6dd8f-449">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
<!--  
<!--    


-->  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Открытие меню команд — команды "выполнить" с помощью меню "команда" Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Приступая к анализу производительности среды выполнения | Документы Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Пример вкладки "действия" | цепь"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors поиска CC-Code"  

> [!NOTE]
> <span data-ttu-id="6dd8f-455">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6dd8f-455">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6dd8f-456">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6dd8f-456">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6dd8f-458">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6dd8f-458">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

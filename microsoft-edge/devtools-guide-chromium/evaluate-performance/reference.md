---
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611750"
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







# <span data-ttu-id="b0e9d-103">Справочные материалы по анализу производительности</span><span class="sxs-lookup"><span data-stu-id="b0e9d-103">Performance Analysis Reference</span></span>   



<span data-ttu-id="b0e9d-104">На этой странице представлен полный справочник по функциям Microsoft Edge DevTools, относящимися к анализу производительности.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="b0e9d-105">Ознакомьтесь [со статьей анализ производительности среды выполнения][DevtoolsEvaluatePerformanceGettingStarted] для учебного руководства по анализу производительности страницы с помощью [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="b0e9d-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="b0e9d-106">Запись производительности</span><span class="sxs-lookup"><span data-stu-id="b0e9d-106">Record performance</span></span>   

### <span data-ttu-id="b0e9d-107">Запись производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="b0e9d-107">Record runtime performance</span></span>   

<span data-ttu-id="b0e9d-108">Записывайте производительность во время выполнения, когда необходимо проанализировать производительность страницы по мере ее выполнения, а не загрузку.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="b0e9d-109">Перейдите на страницу, которую вы хотите проанализировать.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="b0e9d-110">Откройте вкладку **производительность** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="b0e9d-111">Нажмите **кнопку запись** ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-111">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-112">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="b0e9d-112">Figure 1</span></span>  
    > **<span data-ttu-id="b0e9d-113">Record</span><span class="sxs-lookup"><span data-stu-id="b0e9d-113">Record</span></span>**  
    > ![Record][ImageRecord]  

1.  <span data-ttu-id="b0e9d-115">Взаимодействие со страницей.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-115">Interact with the page.</span></span>  <span data-ttu-id="b0e9d-116">DevTools записывает все действия страниц, которые выполняются в результате взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="b0e9d-117">Нажмите кнопку **запись** еще раз или кнопку **остановить** , чтобы остановить запись.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-117">Click **Record** again or click **Stop** to stop recording.</span></span>  

### <span data-ttu-id="b0e9d-118">Скорость загрузки записей</span><span class="sxs-lookup"><span data-stu-id="b0e9d-118">Record load performance</span></span>   

<span data-ttu-id="b0e9d-119">Запишите производительность загрузки, когда необходимо проанализировать производительность страницы при ее загрузке, а не на выполнение.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="b0e9d-120">Перейдите на страницу, которую вы хотите проанализировать.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="b0e9d-121">Откройте панель " **производительность** " DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="b0e9d-122">Нажмите кнопку **Обновить** ![ обновление страницы ][ImageRefreshPageIcon] .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-122">Click **Refresh page** ![Refresh Page][ImageRefreshPageIcon].</span></span>  <span data-ttu-id="b0e9d-123">DevTools записывает метрики производительности во время обновления страницы, а затем автоматически останавливает запись спустя пару секунд после завершения загрузки.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-124">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="b0e9d-124">Figure 2</span></span>  
    > **<span data-ttu-id="b0e9d-125">Обновить страницу</span><span class="sxs-lookup"><span data-stu-id="b0e9d-125">Refresh page</span></span>**  
    > ![Обновить страницу][ImageRefreshPage]  

<span data-ttu-id="b0e9d-127">DevTools автоматически масштабирует часть записи, в которой возникло большинство действий.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-127">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

> ##### <span data-ttu-id="b0e9d-128">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="b0e9d-128">Figure 3</span></span>  
> <span data-ttu-id="b0e9d-129">Запись загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="b0e9d-129">A page-load recording</span></span>  
> ![Запись загрузки страницы][ImageLoadRecording]  

### <span data-ttu-id="b0e9d-131">Снимки экрана при записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-131">Capture screenshots while recording</span></span>   

<span data-ttu-id="b0e9d-132">Установите флажок **снимки экрана** , чтобы зафиксировать снимок экрана для каждого кадра во время записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-132">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

> ##### <span data-ttu-id="b0e9d-133">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="b0e9d-133">Figure 4</span></span>  
> <span data-ttu-id="b0e9d-134">Флажок " **снимки экрана** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-134">The **Screenshots** checkbox</span></span>  
> ![Флажок "снимки экрана"][ImageScreenshots]  

<span data-ttu-id="b0e9d-136">Сведения о том, как работать с снимками экрана, можно найти в разделе [Просмотр снимка экрана](#view-a-screenshot) .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-136">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="b0e9d-137">Принудительная сборка мусора во время записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-137">Force garbage collection while recording</span></span>   

<span data-ttu-id="b0e9d-138">Во время записи страницы выберите команду **собирать** мусорную сборку мусора, ![ ][ImageCollectGarbageIcon] чтобы принудительно выполнить сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-138">While you are recording a page, click **Collect garbage** ![Collect garbage][ImageCollectGarbageIcon] to force garbage collection.</span></span>  

> ##### <span data-ttu-id="b0e9d-139">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="b0e9d-139">Figure 5</span></span>  
> <span data-ttu-id="b0e9d-140">Сбор мусора</span><span class="sxs-lookup"><span data-stu-id="b0e9d-140">Collect garbage</span></span>  
> ![Сбор мусора][ImageCollectGarbage]  

### <span data-ttu-id="b0e9d-142">Показать параметры записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-142">Show recording settings</span></span>   

<span data-ttu-id="b0e9d-143">Нажмите кнопку **захватить** параметры ![ ][ImageCaptureSettingsIcon] , чтобы отобразить дополнительные параметры, связанные с тем, как DevTools захватывает записи производительности.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-143">Click **Capture settings** ![Capture settings][ImageCaptureSettingsIcon] to expose more settings related to how DevTools captures performance recordings.</span></span>  

> ##### <span data-ttu-id="b0e9d-144">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="b0e9d-144">Figure 6</span></span>  
> <span data-ttu-id="b0e9d-145">Раздел " **Параметры захвата** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-145">The **Capture settings** section</span></span>  
> ![Раздел "Параметры захвата"][ImageCaptureSettings]  

### <span data-ttu-id="b0e9d-147">Отключение примеров JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0e9d-147">Disable JavaScript samples</span></span>   

<span data-ttu-id="b0e9d-148">По умолчанию **основной** раздел записи содержит подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-148">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="b0e9d-149">Чтобы отключить эти стеки звонков, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-149">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="b0e9d-150">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-150">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="b0e9d-151">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-151">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="b0e9d-152">Установите флажок **Отключить образцы JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-152">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="b0e9d-153">Запишите страницу.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-153">Take a recording of the page.</span></span>  

<span data-ttu-id="b0e9d-154">[На рис. 7](#figure-7) и [на рисунке 8](#figure-8) показано различие между отключением и включением образцов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-154">[Figure 7](#figure-7) and [Figure 8](#figure-8) show the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="b0e9d-155">**Основной** раздел записи становится более коротким, так как выборка отключена, так как при этом не будут выпускаться все стеки вызовов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-155">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

> ##### <span data-ttu-id="b0e9d-156">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="b0e9d-156">Figure 7</span></span>  
> <span data-ttu-id="b0e9d-157">Пример записи при отключенных примерах JS</span><span class="sxs-lookup"><span data-stu-id="b0e9d-157">An example of a recording when JS samples are disabled</span></span>  
> ![Пример записи при отключенных примерах JS][ImageJSSamplesDisabled]  

> ##### <span data-ttu-id="b0e9d-159">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="b0e9d-159">Figure 8</span></span>  
> <span data-ttu-id="b0e9d-160">Пример записи при включенных примерах JS</span><span class="sxs-lookup"><span data-stu-id="b0e9d-160">An example of a recording when JS samples are enabled</span></span>  
> ![Пример записи при включенных примерах JS][ImageJSSamplesEnabled]  

### <span data-ttu-id="b0e9d-162">Регулирование сети во время записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-162">Throttle the network while recording</span></span>   

<span data-ttu-id="b0e9d-163">Чтобы перерегулировать сеть при записи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-163">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="b0e9d-164">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-164">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="b0e9d-165">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-165">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="b0e9d-166">Настройте **сеть** для нужного уровня регулирования.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-166">Set **Network** to the desired level of throttling.</span></span>  

### <span data-ttu-id="b0e9d-167">Регулирование ЦП во время записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-167">Throttle the CPU while recording</span></span>   

<span data-ttu-id="b0e9d-168">Чтобы перерегулировать ЦП во время записи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-168">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="b0e9d-169">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="b0e9d-170">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="b0e9d-171">Установите для **ЦП** требуемый уровень регулирования.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-171">Set **CPU** to the desired level of throttling.</span></span>  

<span data-ttu-id="b0e9d-172">Регулирование производится относительно возможностей компьютера.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-172">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="b0e9d-173">Например, параметр "интервал по **промедлению** " обеспечивает работу ЦП 2 раза ниже обычного.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-173">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="b0e9d-174">DevTools не имитируют процессоры мобильных устройств, так как архитектура мобильных устройств значительно отличается от настольных компьютеров и ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-174">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="b0e9d-175">Включение расширенного инструментария рисования</span><span class="sxs-lookup"><span data-stu-id="b0e9d-175">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="b0e9d-176">Чтобы просмотреть подробные инструменты для рисования, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-176">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="b0e9d-177">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-177">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="b0e9d-178">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-178">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="b0e9d-179">Установите флажок **включить дополнительные возможности инструментирования краски (медленно)** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-179">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="b0e9d-180">Сведения о том, как взаимодействовать с данными краски, можно найти в статье [Просмотр слоев](#view-layers-information) и [профилировщика Paint](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-180">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="b0e9d-181">Сохранение записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-181">Save a recording</span></span>   

<span data-ttu-id="b0e9d-182">Чтобы сохранить запись, щелкните ее правой кнопкой мыши и выберите команду **Сохранить профиль**.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-182">To save a recording, right-click and select **Save Profile**.</span></span>  

> ##### <span data-ttu-id="b0e9d-183">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="b0e9d-183">Figure 9</span></span>  
> **<span data-ttu-id="b0e9d-184">Сохранить профиль</span><span class="sxs-lookup"><span data-stu-id="b0e9d-184">Save Profile</span></span>**  
> ![Сохранить профиль][ImageSaveProfile]  

## <span data-ttu-id="b0e9d-186">Загрузка записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-186">Load a recording</span></span>   

<span data-ttu-id="b0e9d-187">Чтобы загрузить запись, щелкните ее правой кнопкой мыши и выберите команду " **загрузить профиль**".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-187">To load a recording, right-click and select **Load Profile**.</span></span>  

> ##### <span data-ttu-id="b0e9d-188">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="b0e9d-188">Figure 10</span></span>  
> **<span data-ttu-id="b0e9d-189">Загрузить профиль</span><span class="sxs-lookup"><span data-stu-id="b0e9d-189">Load Profile</span></span>**  
> ![Загрузить профиль][ImageLoadProfile]  

## <span data-ttu-id="b0e9d-191">Удаление предыдущей записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-191">Clear the previous recording</span></span>   

<span data-ttu-id="b0e9d-192">После внесения записи нажмите **Очистить запись** ![ снимите запись, ][ImageClearRecordingIcon] чтобы удалить запись с панели **Performance** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-192">After making a recording, press **Clear recording** ![Clear recording][ImageClearRecordingIcon] to clear that recording from the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="b0e9d-193">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="b0e9d-193">Figure 11</span></span>  
> <span data-ttu-id="b0e9d-194">Очистка записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-194">Clear recording</span></span>  
> ![Очистка записи][ImageClearRecording]  

## <span data-ttu-id="b0e9d-196">Анализ записи производительности</span><span class="sxs-lookup"><span data-stu-id="b0e9d-196">Analyze a performance recording</span></span>   

<span data-ttu-id="b0e9d-197">После того как вы [зарегистрируете производительность во время выполнения](#record-runtime-performance) или [скорость загрузки записи](#record-load-performance), на панели **производительности** можно получить большое количество данных для анализа производительности.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-197">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="b0e9d-198">Выбор части записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-198">Select a portion of a recording</span></span>   

<span data-ttu-id="b0e9d-199">Чтобы выделить часть записи, перетащите указатель мыши по левому или правому краю **обзора** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-199">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="b0e9d-200">**Обзор** — это раздел, содержащий диаграммы в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-200">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="b0e9d-201">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="b0e9d-201">Figure 12</span></span>  
> <span data-ttu-id="b0e9d-202">Перемещение указателя мыши по обзору для изменения масштаба</span><span class="sxs-lookup"><span data-stu-id="b0e9d-202">Dragging the mouse across the Overview to zoom</span></span>  
> ![Перемещение указателя мыши по обзору для изменения масштаба][ImageZoom]  

<span data-ttu-id="b0e9d-204">Чтобы выбрать часть с помощью клавиатуры, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-204">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="b0e9d-205">Щелкните фон **основного** раздела или любой раздел рядом с ним, например **взаимодействия**, **сеть**или **графический процессор**.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-205">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="b0e9d-206">Этот рабочий процесс клавиатуры работает только в том случае, если в фокусе находится один из этих разделов.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-206">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="b0e9d-207">С помощью `W` клавиш,, `A` `S` ,, `D` клавиши для увеличения, перемещения влево, уменьшения и перемещения вправо соответственно.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-207">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="b0e9d-208">Чтобы выбрать часть с помощью сенсорной панели, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-208">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="b0e9d-209">Наведите указатель мыши на раздел **Общие сведения** или на раздел **сведения** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-209">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="b0e9d-210">Раздел **Обзор** — это область, содержащая диаграммы в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-210">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="b0e9d-211">Раздел " **сведения** " — это область, содержащая **основной** раздел, раздел " **взаимодействия** " и т. д.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-211">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="b0e9d-212">С помощью двух пальцев проведите пальцем вверх, проведите пальцем влево, чтобы переместить влево, проведите пальцем вниз, чтобы увеличить масштаб, и проведите пальцем вправо, чтобы перейти вправо.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-212">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="b0e9d-213">Для прокрутки длинной Flame диаграммы в **главном** разделе или любом из соседей щелкните и удерживайте клавишу во время перетаскивания вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-213">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="b0e9d-214">Чтобы переместить выделенную часть записи, перетащите левую и правую клавишу.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-214">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="b0e9d-215">Поиск действий</span><span class="sxs-lookup"><span data-stu-id="b0e9d-215">Search activities</span></span>   

<span data-ttu-id="b0e9d-216">Нажмите клавиши `Control` + `F` \ (Windows \) или `Command` + `F` \ (macOS \), чтобы открыть поле поиска в нижней части панели " **производительность** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-216">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="b0e9d-217">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="b0e9d-217">Figure 13</span></span>  
> <span data-ttu-id="b0e9d-218">Использование Regex в поле поиска в нижней части окна для поиска действий, начинающихся с</span><span class="sxs-lookup"><span data-stu-id="b0e9d-218">Using regex in the search box at the bottom of the window to find any activity that begins with</span></span> `E`  
> ![Поле поиска][ImageSearch]  

<span data-ttu-id="b0e9d-220">Чтобы перейти к действиям, которые соответствуют запросу, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-220">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="b0e9d-221">Используйте кнопки **предыдущий** ![ предыдущий ][ImagePreviousIcon] и **следующий** ![ ниже ][ImageNextIcon] .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-221">Use the **Previous** ![Previous][ImagePreviousIcon] and **Next** ![Next][ImageNextIcon] buttons.</span></span>  
*   <span data-ttu-id="b0e9d-222">Нажмите кнопку, `Shift` + `Enter` чтобы выбрать предыдущую или `Enter` следующую команду.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-222">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="b0e9d-223">Чтобы изменить параметры запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-223">To modify query settings:</span></span>  

*   <span data-ttu-id="b0e9d-224">Нажимайте **клавишу с** учетом регистра ![ ][ImageSearchCaseIcon] , чтобы сделать запрос чувствительным к регистру.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-224">Press **Case sensitive** ![Case sensitive][ImageSearchCaseIcon] to make the query case sensitive.</span></span>  
*   <span data-ttu-id="b0e9d-225">Нажмите **регулярные** ![ выражения Regex ][ImageSearchRegexIcon] , чтобы использовать регулярное выражение в запросе.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-225">Press **Regex** ![Regex][ImageSearchRegexIcon] to use a regular expression in your query.</span></span>  

<span data-ttu-id="b0e9d-226">Чтобы скрыть поле поиска, нажмите кнопку **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-226">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="b0e9d-227">Просмотр основного действия потока</span><span class="sxs-lookup"><span data-stu-id="b0e9d-227">View main thread activity</span></span>   

<span data-ttu-id="b0e9d-228">Используйте **главный** раздел для просмотра действий, которые произошли в основном потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-228">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

> ##### <span data-ttu-id="b0e9d-229">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="b0e9d-229">Figure 14</span></span>  
> <span data-ttu-id="b0e9d-230">**Основной** раздел</span><span class="sxs-lookup"><span data-stu-id="b0e9d-230">The **Main** section</span></span>  
> ![Основной раздел][ImageMain]  

<span data-ttu-id="b0e9d-232">Щелкните событие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .  DevTools выделеет выбранное событие.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-232">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

> ##### <span data-ttu-id="b0e9d-233">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="b0e9d-233">Figure 15</span></span>  
> <span data-ttu-id="b0e9d-234">Дополнительные сведения о `anonymous` функции на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-234">More information about the `anonymous` function in the **Summary** tab</span></span>  
> ![Дополнительные сведения о функции Anonymous на вкладке "Сводка"][ImageMainEventSummary]  

<span data-ttu-id="b0e9d-236">DevTools представляет главную активность потока с Flame диаграммой.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-236">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="b0e9d-237">Ось x обозначает запись с течением времени.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-237">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="b0e9d-238">Ось y представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-238">The y-axis represents the call stack.</span></span>  <span data-ttu-id="b0e9d-239">Событие Top приводит к возникновению событий, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-239">The events on top cause the events below it.</span></span>  

> ##### <span data-ttu-id="b0e9d-240">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="b0e9d-240">Figure 16</span></span>  
> <span data-ttu-id="b0e9d-241">Flame диаграмма в **главном** разделе</span><span class="sxs-lookup"><span data-stu-id="b0e9d-241">A flame chart in the **Main** section</span></span>  
> ![Flame диаграмма][ImageFlameChart]  

<span data-ttu-id="b0e9d-243">На [рисунке 16](#figure-16) `click` событие вызвало `Function Call` в `activitytabs.js` строке 53.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-243">In [Figure 16](#figure-16), a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="b0e9d-244">Ниже `Function Call` показано, что была вызвана анонимная функция.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-244">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="b0e9d-245">Анонимная функция, вызываемая, которая вызывается `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-245">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="b0e9d-246">DevTools назначает сценарии случайные цвета.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-246">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="b0e9d-247">На [рис. 16](#figure-16)вызовы функций из одного сценария окрашены в зеленый цвет.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-247">In [Figure 16](#figure-16), function calls from one script are colored light green.</span></span>  <span data-ttu-id="b0e9d-248">Вызов из другого сценария имеет цветный бежевый.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-248">Calls from another script are colored beige.</span></span>  <span data-ttu-id="b0e9d-249">Темным желтым обозначенными действиями в сценариях, а фиолетовые — действия отрисовки.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-249">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="b0e9d-250">Эти темные желтые и фиолетовые события будут согласованы во всех записях.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-250">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="b0e9d-251">Если вы хотите скрыть подробную flameную диаграмму вызовов JavaScript, просмотрите раздел [Отключение примеров JavaScript](#disable-javascript-samples) .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-251">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="b0e9d-252">При отключенных примерах JS отображаются только события высокого уровня, такие как `Event: click` и `Function Call` на [рисунке 16](#figure-16).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-252">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from [Figure 16](#figure-16).</span></span>  

### <span data-ttu-id="b0e9d-253">Просмотр действий в таблице</span><span class="sxs-lookup"><span data-stu-id="b0e9d-253">View activities in a table</span></span>   

<span data-ttu-id="b0e9d-254">После записи страницы, чтобы проанализировать действия, не нужно полагаться только на **основной** раздел.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-254">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="b0e9d-255">DevTools также предоставляет три табличных представления для анализа действий.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-255">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="b0e9d-256">Каждое представление предлагает различные варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b0e9d-256">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="b0e9d-257">Если вы хотите просмотреть корневые действия, которые приводят к большинству работ, используйте [вкладку " **дерево вызовов** "](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-257">When you want to view the root activities that cause the most work, use [the **Call Tree** tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="b0e9d-258">Если вы хотите просмотреть действия, в которых больше всего потратили время, используйте [вкладку **снизу вверх** ](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-258">When you want to view the activities where the most time was directly spent, use [the **Bottom-Up** tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="b0e9d-259">Если вы хотите просмотреть действия в том порядке, в котором они были обнаружены во время записи, используйте [вкладку **журнал событий** ](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-259">When you want to view the activities in the order in which they occurred during the recording, use [the **Event Log** tab](#the-event-log-tab).</span></span>  

> [!NOTE]
> <span data-ttu-id="b0e9d-260">Следующие три раздела относятся к одной и той же демонстрации.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-260">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="b0e9d-261">Запустите демонстрацию самостоятельно на [вкладке "действия" демонстрации][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="b0e9d-261">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="b0e9d-262">Корневые действия</span><span class="sxs-lookup"><span data-stu-id="b0e9d-262">Root activities</span></span>   

<span data-ttu-id="b0e9d-263">Ниже приведено описание концепции **корневых действий** , упомянутой на вкладке " **дерево вызовов** ", вкладке " **снизу вверх** " и в разделе " **журнал событий** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-263">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="b0e9d-264">Корневые действия — это те, которые приводят к тому, что браузер выполняет определенную работу.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-264">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="b0e9d-265">Например, при щелчке страницы браузер запускает `Event` действие в качестве корневого действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-265">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="b0e9d-266">Это `Event` может привести к запуску обработчика и т. д.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-266">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="b0e9d-267">В диаграмме Flame **основного** раздела корневые действия находятся в верхней части диаграммы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-267">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="b0e9d-268">В **дереве вызовов** и на вкладках **журнал событий** корневые действия — это элементы верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-268">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="b0e9d-269">Пример корневых действий вы видите [на вкладке "дерево вызовов"](#the-call-tree-tab) .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-269">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="b0e9d-270">Вкладка "дерево вызовов"</span><span class="sxs-lookup"><span data-stu-id="b0e9d-270">The Call Tree tab</span></span>   

<span data-ttu-id="b0e9d-271">С помощью вкладки " **дерево вызовов** " можно просмотреть, какие [корневые действия](#root-activities) приводят к наибольшему работоспособности.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-271">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="b0e9d-272">На вкладке " **дерево вызовов** " отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-272">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="b0e9d-273">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-273">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="b0e9d-274">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="b0e9d-274">Figure 17</span></span>  
> <span data-ttu-id="b0e9d-275">Вкладка " **дерево вызовов** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-275">The **Call Tree** tab</span></span>  
> ![Вкладка "дерево вызовов"][ImageCallTree]  

<span data-ttu-id="b0e9d-277">На [рисунке 17](#figure-17)показан верхний уровень элементов в столбце **действие** , `Evaluate Script` а также `Parse HTML` корневые действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-277">In [Figure 17](#figure-17), the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="b0e9d-278">Вложенный объект представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-278">The nesting represents the call stack.</span></span>  <span data-ttu-id="b0e9d-279">Например, на [рисунке 17](#figure-17), `Parse HTML` вызвавшем `Evaluate Script` причины `Compile Script` и `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-279">For example, in [Figure 17](#figure-17), `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="b0e9d-280">**Собственное время** — это время, которое прямо затрачено на это действие.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-280">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="b0e9d-281">**Общее время** представляет время, затраченное на выполнение этого мероприятия или любого из дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-281">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="b0e9d-282">Щелкните **собственное время**, **Общее время**или **активность** , чтобы отсортировать таблицу по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-282">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="b0e9d-283">Используйте текстовое поле " **Фильтр** " для фильтрации событий по имени действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-283">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="b0e9d-284">По умолчанию для меню **Группировка** выбрано значение **Нет группировки**.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-284">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="b0e9d-285">Используйте меню **Группировка** для сортировки таблицы действий на основе различных условий.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-285">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="b0e9d-286">Щелкните **Показать стоп самых тяжелых** ![ ][ImageShowHeaviestStackIcon] , чтобы отобразить другую таблицу справа от таблицы " **действия** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-286">Click **Show Heaviest Stack** ![Show Heaviest Stack][ImageShowHeaviestStackIcon] to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="b0e9d-287">Щелкните действие, чтобы заполнить таблицу с самым **максимальным** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-287">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="b0e9d-288">В таблице наиболее **плотного стека** показано, какие дочерние элементы выбранного действия занимали наибольшее время.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-288">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="b0e9d-289">Вкладка "снизу вверх"</span><span class="sxs-lookup"><span data-stu-id="b0e9d-289">The Bottom-Up tab</span></span>   

<span data-ttu-id="b0e9d-290">С помощью вкладки " **снизу вверх** " можно просмотреть, какие действия немедленно потратили на общее время в агрегате.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-290">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="b0e9d-291">На вкладке " **снизу вверх** " отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-291">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="b0e9d-292">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-292">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="b0e9d-293">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="b0e9d-293">Figure 18</span></span>  
> <span data-ttu-id="b0e9d-294">Вкладка " **снизу вверх** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-294">The **Bottom-Up** tab</span></span>  
> ![Вкладка "снизу вверх"][ImageBottomUp]  

<span data-ttu-id="b0e9d-296">В **главном** разделе Flame [рис. 18](#figure-18)показано, что почти практически все время затрачено на работу `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-296">In the **Main** section flame chart of [Figure 18](#figure-18), see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="b0e9d-297">Верхнее действие на вкладке " **снизу вверх** " на [рисунке 18](#figure-18) `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-297">The top activity in the **Bottom-Up** tab of [Figure 18](#figure-18) is `Parse HTML`.</span></span>  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="b0e9d-298">На вкладке " **снизу вверх** " в списке ниже приведены наиболее ресурсоемкие действия `Layout` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-298">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="b0e9d-299">Столбец " **собственное время** " представляет агрегированное время, проведенное непосредственно в этом действии, для всех вхождений.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-299">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="b0e9d-300">Столбец " **Общее время** " представляет объединенное время, затраченное на это действие или любые дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-300">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="b0e9d-301">Вкладка "журнал событий"</span><span class="sxs-lookup"><span data-stu-id="b0e9d-301">The Event Log tab</span></span>   

<span data-ttu-id="b0e9d-302">Используйте вкладку **журнал событий** , чтобы просмотреть действия в том порядке, в котором они были обнаружены во время записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-302">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="b0e9d-303">На вкладке **журнал событий** отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-303">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="b0e9d-304">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-304">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="b0e9d-305">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="b0e9d-305">Figure 19</span></span>  
> <span data-ttu-id="b0e9d-306">Вкладка " **журнал событий** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-306">The **Event Log** tab</span></span>  
> ![Вкладка "журнал событий"][ImageEventLog]  

<span data-ttu-id="b0e9d-308">Столбец " **время начала** " представляет точку, в которой началось действие, относительно начала записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-308">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="b0e9d-309">Например, время начала `175.7 ms` для выделенного элемента на [рисунке 19](#figure-19) означает, что действие началось 175,7 MS после начала записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-309">For example, the start time of `175.7 ms` for the selected item in [Figure 19](#figure-19) means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="b0e9d-310">Столбец " **собственное время** " представляет время, затраченное непосредственно на это действие.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-310">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="b0e9d-311">Столбцы « **Общее время** » обозначают время, затраченное непосредственно на это действие или в любой из дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-311">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="b0e9d-312">Щелкните **время начала**, **собственное время**или **Общее время** для сортировки таблицы по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-312">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="b0e9d-313">Используйте текстовое поле **Фильтр** , чтобы отфильтровать действия по имени.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-313">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="b0e9d-314">С помощью меню " **Длительность** " можно отфильтровать все действия, которые заняли менее 1 мс или 15 мс.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-314">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="b0e9d-315">По умолчанию для меню **Duration** задано значение **все**, что означает, что отображаются все действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-315">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="b0e9d-316">Отключите флажки " **Загрузка**", " **Создание сценариев**", " **Подготовка**" и " **раскраска** ", чтобы отфильтровать все действия из этих категорий.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-316">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="b0e9d-317">Просмотр действий GPU</span><span class="sxs-lookup"><span data-stu-id="b0e9d-317">View GPU activity</span></span>   

<span data-ttu-id="b0e9d-318">Просматривайте активность GPU в разделе **GPU** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-318">View GPU activity in the **GPU** section.</span></span>  

> ##### <span data-ttu-id="b0e9d-319">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="b0e9d-319">Figure 20</span></span>  
> <span data-ttu-id="b0e9d-320">Раздел **GPU**</span><span class="sxs-lookup"><span data-stu-id="b0e9d-320">The **GPU** section</span></span>  
> ![Раздел GPU][ImageGpu]  

### <span data-ttu-id="b0e9d-322">Просмотр растровых операций</span><span class="sxs-lookup"><span data-stu-id="b0e9d-322">View raster activity</span></span>   

<span data-ttu-id="b0e9d-323">Просматривайте растровые действия в разделе " **растр** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-323">View raster activity in the **Raster** section.</span></span>  

> ##### <span data-ttu-id="b0e9d-324">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="b0e9d-324">Figure 21</span></span>  
> <span data-ttu-id="b0e9d-325">**Разточечный** раздел</span><span class="sxs-lookup"><span data-stu-id="b0e9d-325">The **Raster** section</span></span>  
> ![Разточечный раздел][ImageRaster]  

### <span data-ttu-id="b0e9d-327">Просмотр взаимодействия</span><span class="sxs-lookup"><span data-stu-id="b0e9d-327">View interactions</span></span>   

<span data-ttu-id="b0e9d-328">В разделе " **взаимодействия** " можно найти и проанализировать взаимодействие с пользователями, произошедшие во время записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-328">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

> ##### <span data-ttu-id="b0e9d-329">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="b0e9d-329">Figure 22</span></span>  
> <span data-ttu-id="b0e9d-330">Раздел " **взаимодействия** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-330">The **Interactions** section</span></span>  
> ![Раздел "взаимодействия"][ImageInteractions]  

<span data-ttu-id="b0e9d-332">Красная линия в нижней части взаимодействия представляет время, затраченное на ожидание основного потока.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-332">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="b0e9d-333">Щелкните взаимодействие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-333">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="b0e9d-334">Анализ кадров в секунду (кадр/с)</span><span class="sxs-lookup"><span data-stu-id="b0e9d-334">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="b0e9d-335">DevTools предлагает многочисленные способы анализа кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-335">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="b0e9d-336">Используйте [диаграмму в **кадре** ](#the-fps-chart) , чтобы получить обзор кадров в кадре в течение не более чем на продолжительность записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-336">Use [the **FPS** chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="b0e9d-337">С помощью [раздела **кадры** ](#the-frames-section) вы можете узнать, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-337">Use [the **Frames** section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="b0e9d-338">Используйте **индикатор кадров между кадрами** для оценки в режиме реального времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-338">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="b0e9d-339">Показать [количество кадров в секунду в режиме реального времени с индикатором кадров](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-339">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  

#### <span data-ttu-id="b0e9d-340">Диаграмма кадр/с</span><span class="sxs-lookup"><span data-stu-id="b0e9d-340">The FPS chart</span></span>   

<span data-ttu-id="b0e9d-341">Диаграмма **кадр/** с — это обзор частоты кадров во время записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-341">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="b0e9d-342">Как правило, чем больше зеленая полоса, тем выше частота кадров.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-342">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="b0e9d-343">Красная черта над диаграммой с индикатором **кадров** — это предупреждение о том, что частота кадров отброшена настолько, что она может повредить взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-343">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

> ##### <span data-ttu-id="b0e9d-344">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="b0e9d-344">Figure 23</span></span>  
> <span data-ttu-id="b0e9d-345">Диаграмма кадр/с</span><span class="sxs-lookup"><span data-stu-id="b0e9d-345">The FPS chart</span></span>  
> ![Диаграмма кадр/с][ImageFpsChart]  

#### <span data-ttu-id="b0e9d-347">Раздел "кадры"</span><span class="sxs-lookup"><span data-stu-id="b0e9d-347">The Frames section</span></span>   

<span data-ttu-id="b0e9d-348">Раздел **кадры** содержит сведения о том, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-348">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="b0e9d-349">Наведите указатель мыши на кадр, чтобы просмотреть всплывающую подсказку с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-349">Hover over a frame to view a tooltip with more information about it.</span></span>  

> ##### <span data-ttu-id="b0e9d-350">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="b0e9d-350">Figure 24</span></span>  
> <span data-ttu-id="b0e9d-351">Наведение указателя мыши на рамку</span><span class="sxs-lookup"><span data-stu-id="b0e9d-351">Hovering over a frame</span></span>  
> ![Наведение указателя мыши на рамку][ImageFramesSection]  

<span data-ttu-id="b0e9d-353">Щелкните рамку, чтобы просмотреть дополнительные сведения о кадре на вкладке " **Сводка** ".  DevTools выделеет выделенный кадр синим цветом.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-353">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

> ##### <span data-ttu-id="b0e9d-354">Рис. 25</span><span class="sxs-lookup"><span data-stu-id="b0e9d-354">Figure 25</span></span>  
> <span data-ttu-id="b0e9d-355">Просмотр кадра на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-355">Viewing a frame in the **Summary** tab</span></span>  
> ![Просмотр кадра на вкладке "Сводка"][ImageFrameSummary]  

### <span data-ttu-id="b0e9d-357">Просмотр сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="b0e9d-357">View network requests</span></span>   

<span data-ttu-id="b0e9d-358">Разверните раздел **сеть** , чтобы просмотреть каскадные сетевые запросы, которые произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-358">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

> ##### <span data-ttu-id="b0e9d-359">Рис. 26</span><span class="sxs-lookup"><span data-stu-id="b0e9d-359">Figure 26</span></span>  
> <span data-ttu-id="b0e9d-360">Раздел " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-360">The **Network** section</span></span>  
> ![Раздел "сеть"][ImageNetworkRequest]  

<span data-ttu-id="b0e9d-362">Запросы записываются цветом следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b0e9d-362">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="b0e9d-363">HTML: синий</span><span class="sxs-lookup"><span data-stu-id="b0e9d-363">HTML: Blue</span></span>  
*   <span data-ttu-id="b0e9d-364">CSS: фиолетовый</span><span class="sxs-lookup"><span data-stu-id="b0e9d-364">CSS: Purple</span></span>  
*   <span data-ttu-id="b0e9d-365">JS: желтый</span><span class="sxs-lookup"><span data-stu-id="b0e9d-365">JS: Yellow</span></span>  
*   <span data-ttu-id="b0e9d-366">Изображения: зеленые</span><span class="sxs-lookup"><span data-stu-id="b0e9d-366">Images: Green</span></span>  

<span data-ttu-id="b0e9d-367">Щелкните запрос, чтобы просмотреть дополнительные сведения о нем на вкладке " **Сводка** ".  Например, на [рисунке 26](#figure-26) на вкладке " **Сводка** " отображаются дополнительные сведения о синем запросе, выбранном в разделе " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-367">Click on a request to view more information about it in the **Summary** tab.  For example, in [Figure 26](#figure-26) the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="b0e9d-368">Темно-синий квадрат в верхней левой части запроса означает, что это запрос более высокого приоритета.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-368">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="b0e9d-369">Более светлый квадрат — более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-369">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="b0e9d-370">Например, на [рисунке 26](#figure-26) синей, выбранный запрос имеет более высокий приоритет, а зеленый — более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-370">For example, in [Figure 26](#figure-26) the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="b0e9d-371">На [рисунке 27](#figure-27)запрос представляется `www.bing.com` линией слева, полосой в середине, темной частью и светлым фрагментом, а также линией справа.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-371">In [Figure 27](#figure-27), the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="b0e9d-372">На [рисунке 28](#figure-28) показано соответствующее представление того же запроса на вкладке **время** на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-372">[Figure 28](#figure-28) shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="b0e9d-373">Ниже показано, как эти два представления соотносятся друг с другом.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-373">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="b0e9d-374">Левая строка — это все, что нужно для `Connection Start` группы событий (включительно).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-374">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="b0e9d-375">Другими словами, это все, что раньше `Request Sent` , исключительно.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-375">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="b0e9d-376">Светлая часть панели — `Request Sent` и `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-376">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="b0e9d-377">Темная часть панели `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-377">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="b0e9d-378">В настоящее время в течение всего времени, затраченного на ожидание основного потока, в правой строке.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-378">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="b0e9d-379">Этот параметр не отображается на вкладке **время** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-379">This is not represented in the **Timing** tab.</span></span>  

> ##### <span data-ttu-id="b0e9d-380">На рисунке 27</span><span class="sxs-lookup"><span data-stu-id="b0e9d-380">Figure 27</span></span>  
> <span data-ttu-id="b0e9d-381">Представление запроса в виде строки на строке `www.bing.com`</span><span class="sxs-lookup"><span data-stu-id="b0e9d-381">The line-bar representation of the `www.bing.com` request</span></span>  
> ![Представление строки запроса www.bing.com в виде линейчатой диаграммы][ImageLineBar]  

> ##### <span data-ttu-id="b0e9d-383">Рис. 28</span><span class="sxs-lookup"><span data-stu-id="b0e9d-383">Figure 28</span></span>  
> <span data-ttu-id="b0e9d-384">Представление запроса с вкладкой " **время** " `www.bing.com`</span><span class="sxs-lookup"><span data-stu-id="b0e9d-384">The **Timing** tab representation of the `www.bing.com` request</span></span>  
> ![Раздел "сеть"][ImageTiming]  

### <span data-ttu-id="b0e9d-386">Просмотр метрик памяти</span><span class="sxs-lookup"><span data-stu-id="b0e9d-386">View memory metrics</span></span>   

<span data-ttu-id="b0e9d-387">Включите флажок **память** , чтобы просмотреть метрики памяти от последней записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-387">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

> ##### <span data-ttu-id="b0e9d-388">Рис. 29</span><span class="sxs-lookup"><span data-stu-id="b0e9d-388">Figure 29</span></span>  
> <span data-ttu-id="b0e9d-389">Флажок " **память** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-389">The **Memory** checkbox</span></span>  
> ![Флажок "память"][ImageMemory]  

<span data-ttu-id="b0e9d-391">DevTools выводит новую диаграмму с **памятью** над вкладкой **Сводка** .  Кроме того, вы также можете создать новую диаграмму под **чистой** диаграммой, называемой **кучей**.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-391">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="b0e9d-392">Диаграмма **кучи** предоставляет те же данные, что и в линии **кучи JS** в диаграмме с **памятью** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-392">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

> ##### <span data-ttu-id="b0e9d-393">Рис. 30</span><span class="sxs-lookup"><span data-stu-id="b0e9d-393">Figure 30</span></span>  
> <span data-ttu-id="b0e9d-394">Метрики памяти над вкладкой " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-394">Memory metrics, above the **Summary** tab</span></span>  
> ![Метрики памяти][ImageMemoryMetrics]  

<span data-ttu-id="b0e9d-396">Цветные линии на диаграмме сопоставляются с цветными флажками над диаграммой.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-396">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="b0e9d-397">Отключите флажок, чтобы скрыть эту категорию на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-397">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="b0e9d-398">На диаграмме отображается только область текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-398">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="b0e9d-399">Например, на [рисунке 30](#figure-30)диаграмма " **память** " показывает использование памяти только вокруг 400 MS, помечая его на 1750 MS.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-399">For example, in [Figure 30](#figure-30), the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="b0e9d-400">Просмотр длительности части записи</span><span class="sxs-lookup"><span data-stu-id="b0e9d-400">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="b0e9d-401">При анализе раздела, например " **сеть** " или " **основной**", иногда требуется более точная оценка продолжительности определенных событий.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-401">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="b0e9d-402">`Shift`Чтобы выделить часть записи, перетащите указатель влево или вправо, удерживая нажатой клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-402">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="b0e9d-403">В нижней части выделенного фрагмента DevTools показывает, сколько времени заняло эта часть.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-403">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

> ##### <span data-ttu-id="b0e9d-404">На рисунке 31</span><span class="sxs-lookup"><span data-stu-id="b0e9d-404">Figure 31</span></span>  
> <span data-ttu-id="b0e9d-405">`9.47ms`Метка времени в нижней части выбранной части указывает, сколько времени потребовалось</span><span class="sxs-lookup"><span data-stu-id="b0e9d-405">The `9.47ms` timestamp at the bottom of the selected portion indicates how long that portion took</span></span>  
> ![Просмотр длительности части записи][ImageDuration]  

### <span data-ttu-id="b0e9d-407">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="b0e9d-407">View a screenshot</span></span>   

<span data-ttu-id="b0e9d-408">Сведения о включении снимков экрана можно найти в разделе [запись снимков экрана](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-408">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="b0e9d-409">Наведите указатель мыши на **Обзор** , чтобы просмотреть снимок экрана, на котором размещается страница в этот момент записи.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-409">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="b0e9d-410">**Обзор** — это раздел, содержащий диаграммы **ЦП**, **кадров между кадрами**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-410">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="b0e9d-411">Рисунок 32</span><span class="sxs-lookup"><span data-stu-id="b0e9d-411">Figure 32</span></span>  
> <span data-ttu-id="b0e9d-412">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="b0e9d-412">Viewing a screenshot</span></span>  
> ![Просмотр снимка экрана][ImageViewScreenshot]  

<span data-ttu-id="b0e9d-414">Вы также можете просмотреть снимки экрана, щелкнув кадр в разделе **кадры** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-414">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="b0e9d-415">DevTools отображает маленькую версию снимка экрана на вкладке " **Сводка** ".</span><span class="sxs-lookup"><span data-stu-id="b0e9d-415">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

> ##### <span data-ttu-id="b0e9d-416">Рисунок 33</span><span class="sxs-lookup"><span data-stu-id="b0e9d-416">Figure 33</span></span>  
> <span data-ttu-id="b0e9d-417">После щелчка `233.9ms` кадра в разделе " **кадры** " на вкладке " **Сводка** " отображается снимок экрана для этого кадра.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-417">After clicking the `233.9ms` frame in the **Frames** section, the screenshot for that frame is displayed in the **Summary** tab</span></span>  
> ![Просмотр снимка экрана на вкладке "Сводка"][ImageFrameScreenshotSummary]  

<span data-ttu-id="b0e9d-419">Щелкните эскиз на вкладке " **Сводка** ", чтобы увеличить масштаб на снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-419">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

> ##### <span data-ttu-id="b0e9d-420">Рисунок 34</span><span class="sxs-lookup"><span data-stu-id="b0e9d-420">Figure 34</span></span>  
> <span data-ttu-id="b0e9d-421">После того как вы щелкните эскиз на вкладке " **Сводка** ", DevTools увеличит масштаб экрана</span><span class="sxs-lookup"><span data-stu-id="b0e9d-421">After clicking the thumbnail in the **Summary** tab, DevTools zooms in on the screenshot</span></span>  
> ![Изменение масштаба снимка экрана с вкладки "Сводка"][ImageFrameScreenshotZoom]  

### <span data-ttu-id="b0e9d-423">Просмотр сведений о слоях</span><span class="sxs-lookup"><span data-stu-id="b0e9d-423">View layers information</span></span>   

<span data-ttu-id="b0e9d-424">Чтобы просмотреть дополнительные сведения о кадре, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-424">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="b0e9d-425">[Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-425">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="b0e9d-426">Выберите кадр в разделе **кадры** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-426">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="b0e9d-427">DevTools отображает сведения о слоях на вкладке Создание **слоев** рядом с вкладкой **журнал событий** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-427">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-428">Рисунок 35</span><span class="sxs-lookup"><span data-stu-id="b0e9d-428">Figure 35</span></span>  
    > <span data-ttu-id="b0e9d-429">Область **слоев**</span><span class="sxs-lookup"><span data-stu-id="b0e9d-429">The **Layers** pane</span></span>  
    > ![Область слоев][ImageLayers]  
    
<span data-ttu-id="b0e9d-431">Наведите указатель мыши на слой, чтобы выделить его на схеме.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-431">Hover over a layer to highlight it in the diagram.</span></span>  

> ##### <span data-ttu-id="b0e9d-432">Рисунок 36</span><span class="sxs-lookup"><span data-stu-id="b0e9d-432">Figure 36</span></span>  
> <span data-ttu-id="b0e9d-433">Выделение **#39** слоев</span><span class="sxs-lookup"><span data-stu-id="b0e9d-433">Highlighting layer **#39**</span></span>  
> ![Выделение слоя][ImageLayerHover]  

<span data-ttu-id="b0e9d-435">Чтобы переместить схему, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-435">To move the diagram:</span></span>  

*   <span data-ttu-id="b0e9d-436">Щелкните режим **панорамирования** , ![ ][ImagePanModeIcon] чтобы переместиться вдоль осей X и Y.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-436">Click **Pan Mode** ![Pan Mode][ImagePanModeIcon] to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="b0e9d-437">Нажмите режим поворота **режима** ![ поворота ][ImageRotateModeIcon] для поворота вдоль оси Z.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-437">Click **Rotate Mode** ![Rotate Mode][ImageRotateModeIcon] to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="b0e9d-438">Нажмите кнопку **Сброс** ![ преобразования сброса преобразования ][ImageResetTransformIcon] , чтобы восстановить исходное расположение схемы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-438">Click **Reset Transform** ![Reset Transform][ImageResetTransformIcon] to reset the diagram to the original position.</span></span>  

### <span data-ttu-id="b0e9d-439">Просмотр профилировщика Paint</span><span class="sxs-lookup"><span data-stu-id="b0e9d-439">View paint profiler</span></span>   

<span data-ttu-id="b0e9d-440">Чтобы просмотреть дополнительные сведения о событии Paint, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-440">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="b0e9d-441">[Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-441">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="b0e9d-442">Выберите событие **Paint** в **главном** разделе.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-442">Select a **Paint** event in the **Main** section.</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-443">Рисунок 37</span><span class="sxs-lookup"><span data-stu-id="b0e9d-443">Figure 37</span></span>  
    > <span data-ttu-id="b0e9d-444">Вкладка " **профилировщик Paint** "</span><span class="sxs-lookup"><span data-stu-id="b0e9d-444">The **Paint Profiler** tab</span></span>  
    > ![Вкладка "профилировщик Paint"][ImagePaintProfiler]  
    
## <span data-ttu-id="b0e9d-446">Анализ производительности отрисовки с помощью вкладки "рендеринг"</span><span class="sxs-lookup"><span data-stu-id="b0e9d-446">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="b0e9d-447">С помощью функций вкладки " **отрисовка** " можно визуализировать эффективность отрисовки страницы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-447">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="b0e9d-448">Чтобы открыть вкладку **рендеринга** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-448">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="b0e9d-449">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="b0e9d-449">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="b0e9d-450">Начните вводить текст `Rendering` и выберите его `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-450">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="b0e9d-451">DevTools отображает вкладку **рендеринг** в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-451">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-452">Рисунок 38</span><span class="sxs-lookup"><span data-stu-id="b0e9d-452">Figure 38</span></span>  
    > <span data-ttu-id="b0e9d-453">Вкладка « **рендеринг** »</span><span class="sxs-lookup"><span data-stu-id="b0e9d-453">The **Rendering** tab</span></span>  
    > ![Вкладка «рендеринг»][ImageRenderingTab]  
    
### <span data-ttu-id="b0e9d-455">Просмотр кадров в секунду в режиме реального времени с индикатором кадров</span><span class="sxs-lookup"><span data-stu-id="b0e9d-455">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="b0e9d-456">**Индикатор кадров в кадрах** — это наложение, которое отображается в правом верхнем углу окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-456">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="b0e9d-457">Она предоставляет оценку кадров в реальном времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-457">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="b0e9d-458">Чтобы открыть **индикатор кадров**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-458">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="b0e9d-459">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-459">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="b0e9d-460">Включите флажок **индикатор кадров в кадре** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-460">Enable the **FPS Meter** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-461">Рисунок 39</span><span class="sxs-lookup"><span data-stu-id="b0e9d-461">Figure 39</span></span>  
    > <span data-ttu-id="b0e9d-462">Индикатор кадров в кадре</span><span class="sxs-lookup"><span data-stu-id="b0e9d-462">The FPS meter</span></span>  
    > ![Индикатор кадров в кадре][ImageFpsMeter]  
    
### <span data-ttu-id="b0e9d-464">Просмотр событий рисования в реальном времени с помощью помигания Paint</span><span class="sxs-lookup"><span data-stu-id="b0e9d-464">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="b0e9d-465">Чтобы получить представление о всех событиях рисования на странице в реальном времени, используйте Paint.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-465">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="b0e9d-466">Каждый раз, когда часть страницы зарисуется повторно, DevTools разменяет его зеленым цветом.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-466">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="b0e9d-467">Чтобы включить мигание краски, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="b0e9d-467">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="b0e9d-468">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-468">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="b0e9d-469">Установите флажок **закрасить мигающий** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-469">Enable the **Paint Flashing** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-470">Рисунок 40</span><span class="sxs-lookup"><span data-stu-id="b0e9d-470">Figure 40</span></span>  
    > **<span data-ttu-id="b0e9d-471">Мигание краски</span><span class="sxs-lookup"><span data-stu-id="b0e9d-471">Paint Flashing</span></span>**  
    > ![Мигание краски][ImagePaintFlashing]  
    
### <span data-ttu-id="b0e9d-473">Просмотр наложения слоев с границами слоев</span><span class="sxs-lookup"><span data-stu-id="b0e9d-473">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="b0e9d-474">Используйте **границы слоев** для просмотра наложенных границ слоев и плиток в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-474">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="b0e9d-475">Чтобы включить границы слоев, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-475">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="b0e9d-476">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-476">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="b0e9d-477">Установите флажок **границы слоя** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-477">Enable the **Layer Borders** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="b0e9d-478">Рисунок 41</span><span class="sxs-lookup"><span data-stu-id="b0e9d-478">Figure 41</span></span>  
    > **<span data-ttu-id="b0e9d-479">Границы слоев</span><span class="sxs-lookup"><span data-stu-id="b0e9d-479">Layer Borders</span></span>**  
    > ![Границы слоев][ImageLayerBorders]  
    
<span data-ttu-id="b0e9d-481">Ознакомьтесь с комментариями [`debug_colors.cc`][ChromiumDebugColors] , изложенными в разделе Описание цветовых кодирования.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-481">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="b0e9d-482">Поиск проблем с производительностью прокрутки в реальном времени</span><span class="sxs-lookup"><span data-stu-id="b0e9d-482">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="b0e9d-483">Используйте проблемы с производительностью прокрутки, чтобы идентифицировать элементы страницы, которые содержат прослушиватели событий, связанные с прокруткой, которые могут повредить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-483">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="b0e9d-484">DevTools поменяет потенциально проблематичные элементы в синем тексте.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-484">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="b0e9d-485">Для просмотра проблем с производительностью прокрутки:</span><span class="sxs-lookup"><span data-stu-id="b0e9d-485">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="b0e9d-486">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-486">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="b0e9d-487">Включите флажок **проблемы с прокруткой** .</span><span class="sxs-lookup"><span data-stu-id="b0e9d-487">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
 
    > ##### <span data-ttu-id="b0e9d-488">Рисунок 42</span><span class="sxs-lookup"><span data-stu-id="b0e9d-488">Figure 42</span></span>  
    > <span data-ttu-id="b0e9d-489">**Прокрутка проблем с производительностью** указывает на то, что объекты просмотра, не связанные с разслойю, могут повредить производительность при прокрутке.</span><span class="sxs-lookup"><span data-stu-id="b0e9d-489">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    > ![Прокрутка проблем с производительностью указывает на то, что объекты просмотра, не связанные с разслойю, могут повредить производительность при прокрутке.][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Рисунок 1: запись"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Рисунок 2: обновление страницы"  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Рисунок 3: запись загрузки страницы"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Рисунок 4: флажок снимки экрана"  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Рисунок 5: сбор мусора"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Рисунок 6: раздел "Параметры захвата""  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Рисунок 7: пример записи при отключенных примерах JS"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Рисунок 8: пример записи при включенных примерах JS"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Рисунок 9: сохранение профиля"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Рисунок 10: Загрузка профиля"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Рисунок 11: Очистка записи"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Рисунок 12: перетаскивание указателя мыши по обзору для изменения масштаба"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Рисунок 13: поле поиска"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Рисунок 14: основной раздел"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Рисунок 15: Дополнительные сведения о функции Anonymous на вкладке "Сводка""  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Рисунок 16: Flame диаграмма"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Рисунок 17: вкладка "дерево вызовов""  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Рисунок 18: вкладка "снизу вверх""  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "На рисунке 19 показана вкладка Журнал событий."  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Рисунок 20: раздел GPU"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Рисунок 21: точечный раздел"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Рисунок 22: раздел "взаимодействия""  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Рисунок 23: диаграмма кадр/с"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Рисунок 24: наведение указателя на рамку"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Рисунок 25: просмотр кадра на вкладке "Сводка""  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Рисунок 26: раздел сеть"  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Рисунок 27: линейное представление запроса www.bing.com"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Рисунок 28: раздел сеть"  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Рисунок 29: флажок "память""  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Рис. 30: метрики памяти"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Рисунок 31: Просмотр длительности части записи"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Рисунок 32: Просмотр снимка экрана"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Рисунок 33: Просмотр снимка экрана на вкладке "Сводка""  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Рисунок 34: масштабирование снимков экрана на вкладке "Сводка""  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Рисунок 35: область "слои""  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Рисунок 36: выделение слоя"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Рисунок 37: вкладка "профилировщик Paint""  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Рисунок 38: вкладка «рендеринг»"  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Рисунок 39: индикатор кадров в кадре"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Рисунок 40: мигает графический редактор"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Рисунок 41: границы слоев"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Рисунок 42: прокрутка проблем с производительностью указывает на то, что объекты просмотра, не связанные с разслойю, могут повредить производительность при прокрутке."  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Открытие меню команд: команды "выполнить" с помощью меню Microsoft Edge DevTools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Приступая к анализу производительности среды выполнения"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Пример вкладок "действия""  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors поиска CC-Code"  

> [!NOTE]
> <span data-ttu-id="b0e9d-538">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0e9d-538">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b0e9d-539">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b0e9d-539">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b0e9d-541">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0e9d-541">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

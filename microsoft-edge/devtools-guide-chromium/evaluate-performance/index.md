---
title: Приступая к анализу производительности среды выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611743"
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







# <span data-ttu-id="50fd3-103">Приступая к анализу производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="50fd3-103">Get Started With Analyzing Runtime Performance</span></span>   



> [!NOTE]
> <span data-ttu-id="50fd3-104">Сведения о том, как ускорить загрузку страниц, можно найти в разделе [Оптимизация веб-сайта][DevtoolsSpeedGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="50fd3-104">See [Optimize Website Speed][DevtoolsSpeedGetStarted] to learn how to make your pages load faster.</span></span>  

<span data-ttu-id="50fd3-105">Производительность во время выполнения — это то, как страница выполняется при ее запуске, а не в виде загрузки.</span><span class="sxs-lookup"><span data-stu-id="50fd3-105">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="50fd3-106">В этом учебнике объясняется, как использовать панель производительности Microsoft Edge DevTools для анализа производительности среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="50fd3-106">This tutorial teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="50fd3-107">В плане модели **салазок** уровни опыта, описанные в этом учебнике, полезны для анализа отклика, анимации и этапов простоя страницы.</span><span class="sxs-lookup"><span data-stu-id="50fd3-107">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="50fd3-108">Начало работы</span><span class="sxs-lookup"><span data-stu-id="50fd3-108">Get started</span></span>   

<span data-ttu-id="50fd3-109">В этом учебнике вы откроете DevTools на реальной странице и с помощью панели Performance (производительность) найдите узкие места в производительности на странице.</span><span class="sxs-lookup"><span data-stu-id="50fd3-109">In this tutorial, you open DevTools on a live page and use the Performance panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="50fd3-110">Откройте Microsoft EDGE в **режиме InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-110">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="50fd3-111">Режим InPrivate обеспечивает выполнение Microsoft EDGE в чистом состоянии.</span><span class="sxs-lookup"><span data-stu-id="50fd3-111">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="50fd3-112">Например, если на вашем компьютере установлено большое количество расширений, это может привести к снижению производительности с помощью этих расширений.</span><span class="sxs-lookup"><span data-stu-id="50fd3-112">For example, if you have a lot of extensions installed, those extensions might create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="50fd3-113">Загрузите следующую страницу в окне InPrivate.</span><span class="sxs-lookup"><span data-stu-id="50fd3-113">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="50fd3-114">Это демонстрационный ролик, для которого вы собираетесь профилировать.</span><span class="sxs-lookup"><span data-stu-id="50fd3-114">This is the demo that you're going to profile.</span></span>  <span data-ttu-id="50fd3-115">На странице показан ряд маленьких значков, перемещаясь вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="50fd3-115">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  <span data-ttu-id="50fd3-116">`Control` + `Shift` + `I` Чтобы открыть DevTools, нажмите клавиши \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="50fd3-116">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-117">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="50fd3-117">Figure 1</span></span>  
    > <span data-ttu-id="50fd3-118">Демонстрация слева и DevTools справа</span><span class="sxs-lookup"><span data-stu-id="50fd3-118">The demo on the left, and DevTools on the right</span></span>  
    > ![Демонстрация слева и DevTools справа][ImageGetStarted]  
    
    > [!NOTE]
    > <span data-ttu-id="50fd3-120">Для остальных снимков DevTools [отсоединяется в отдельном окне][DevtoolsCustomizePlacement] , и вы сможете лучше видеть содержимое.</span><span class="sxs-lookup"><span data-stu-id="50fd3-120">For the rest of the screenshots, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] so that you can see the contents better.</span></span>  
    
### <span data-ttu-id="50fd3-121">Имитация мобильного ЦП</span><span class="sxs-lookup"><span data-stu-id="50fd3-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="50fd3-122">На мобильных устройствах больше энергии ЦП, чем на настольных компьютерах и ноутбуках.</span><span class="sxs-lookup"><span data-stu-id="50fd3-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="50fd3-123">Каждый раз, когда вы профилем страницы, используйте метод регулирования ЦП для моделирования того, как страница работает на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="50fd3-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="50fd3-124">В DevTools откройте вкладку **производительность** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-124">In DevTools, click the **Performance** tab.</span></span>  
1.  <span data-ttu-id="50fd3-125">Убедитесь, что флажок **снимки экрана** включен.</span><span class="sxs-lookup"><span data-stu-id="50fd3-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="50fd3-126">Нажмите кнопку Параметры захвата **параметров** ![ ][ImageCaptureSettingsIcon] .</span><span class="sxs-lookup"><span data-stu-id="50fd3-126">Click **Capture Settings** ![Capture Settings][ImageCaptureSettingsIcon].</span></span>  <span data-ttu-id="50fd3-127">DevTools показывает параметры, связанные с тем, как они захватывают метрики производительности.</span><span class="sxs-lookup"><span data-stu-id="50fd3-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="50fd3-128">На вкладке **ЦП**выберите пункт **замедление 4X**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-128">For **CPU**, select **4x slowdown**.</span></span>  <span data-ttu-id="50fd3-129">DevTools загружает ЦП так, чтобы он был 4 медленнее, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="50fd3-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-130">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="50fd3-130">Figure 2</span></span>  
    > <span data-ttu-id="50fd3-131">Регулировка скорости ЦП</span><span class="sxs-lookup"><span data-stu-id="50fd3-131">CPU throttling</span></span>  
    > ![Регулировка скорости ЦП][ImageCPUThrottling]  
    
    > [!NOTE]
    > <span data-ttu-id="50fd3-133">При тестировании других страниц, чтобы убедиться в том, что они работают на мобильных устройствах с низким энергопотреблением, настройте для ускорения ЦП **6X замедление**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-133">When testing other pages, if you want to ensure that they work well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="50fd3-134">Эта демонстрация не подходит для 6xного замедления, поэтому она просто использует 4X замедления для целей обучения.</span><span class="sxs-lookup"><span data-stu-id="50fd3-134">This demo doesn't work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="50fd3-135">Настройка ролика</span><span class="sxs-lookup"><span data-stu-id="50fd3-135">Set up the demo</span></span>  

<span data-ttu-id="50fd3-136">Очень сложно создать демонстрацию производительности во время выполнения, который постоянно подходит всем читателям этого веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="50fd3-136">It is hard to create a runtime performance demo that works consistently for all readers of this website.</span></span>  <span data-ttu-id="50fd3-137">Этот раздел позволяет настроить демонстрацию, чтобы убедиться в том, что взаимодействие с изображениями и описаниями, которые вы видите в этом учебнике, не зависит от настройки.</span><span class="sxs-lookup"><span data-stu-id="50fd3-137">This section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions you see in this tutorial, regardless of your particular setup.</span></span>

1.  <span data-ttu-id="50fd3-138">Продолжайте нажимать кнопку " **Добавить 10** ", пока синие значки не перемещаются заметно ниже.</span><span class="sxs-lookup"><span data-stu-id="50fd3-138">Keep clicking **Add 10** until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="50fd3-139">На высоком уровне компьютера может потребоваться около 20 щелчков мыши.</span><span class="sxs-lookup"><span data-stu-id="50fd3-139">On a high-end machine, it may take about 20 clicks.</span></span>  
1.  <span data-ttu-id="50fd3-140">Нажмите кнопку **оптимизировать**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-140">Click **Optimize**.</span></span>  <span data-ttu-id="50fd3-141">Синие значки должны двигаться быстрее и более гладко.</span><span class="sxs-lookup"><span data-stu-id="50fd3-141">The blue icons should move faster and more smoothly.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="50fd3-142">Если вы не видите заметную разницу между оптимизированными и неоптимизированными версиями, попробуйте выбрать команду **вычесть 10** несколько раз и повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="50fd3-142">If you don't see a noticeable difference between the optimized and un-optimized versions, try clicking **Subtract 10** a few times and trying again.</span></span>  
    > <span data-ttu-id="50fd3-143">Если вы добавите слишком много синих значков, вы просто сможете максимально использовать ЦП, и вы не будете видеть существенные различия в результатах двух версий.</span><span class="sxs-lookup"><span data-stu-id="50fd3-143">If you add too many blue icons, you're just going to max out the CPU and you're not going to see a major difference in the results for the two versions.</span></span>  

1.  <span data-ttu-id="50fd3-144">Нажмите **Отмена оптимизации**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-144">Click **Un-Optimize**.</span></span>  <span data-ttu-id="50fd3-145">Синие значки перемещаются медленнее и более Jank еще раз.</span><span class="sxs-lookup"><span data-stu-id="50fd3-145">The blue icons move slower and with more jank again.</span></span>  

### <span data-ttu-id="50fd3-146">Запись производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="50fd3-146">Record runtime performance</span></span>   

<span data-ttu-id="50fd3-147">Когда вы запустили оптимизированную версию страницы, синие значки перемещаются быстрее.</span><span class="sxs-lookup"><span data-stu-id="50fd3-147">When you ran the optimized version of the page, the blue icons move faster.</span></span>  
<span data-ttu-id="50fd3-148">Почему так?</span><span class="sxs-lookup"><span data-stu-id="50fd3-148">Why is that?</span></span>  <span data-ttu-id="50fd3-149">Обе версии предназначены для того, чтобы переместить значки в одинаковые промежутки времени.</span><span class="sxs-lookup"><span data-stu-id="50fd3-149">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="50fd3-150">Чтобы выяснить, как выявить узкие места производительности в неоптимизированной версии, сделайте запись на панели производительности.</span><span class="sxs-lookup"><span data-stu-id="50fd3-150">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="50fd3-151">В **DevTools нажмите запись Record (запись)** ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="50fd3-151">In DevTools, click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="50fd3-152">DevTools захватывает метрики производительности по мере выполнения страницы.</span><span class="sxs-lookup"><span data-stu-id="50fd3-152">DevTools captures performance metrics as the page runs.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-153">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="50fd3-153">Figure 3</span></span> 
    > <span data-ttu-id="50fd3-154">Профилирование страницы</span><span class="sxs-lookup"><span data-stu-id="50fd3-154">Profiling the page</span></span>  
    > ![Профилирование страницы][ImagePageProfiling]  
    
1.  <span data-ttu-id="50fd3-156">Подождите несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="50fd3-156">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="50fd3-157">Нажмите кнопку **остановить**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-157">Click **Stop**.</span></span>  <span data-ttu-id="50fd3-158">DevTools останавливает запись, обрабатывает данные, а затем отображает результаты на панели Performance.</span><span class="sxs-lookup"><span data-stu-id="50fd3-158">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-159">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="50fd3-159">Figure 4</span></span>  
    > <span data-ttu-id="50fd3-160">Результаты профиля</span><span class="sxs-lookup"><span data-stu-id="50fd3-160">The results of the profile</span></span>  
    > ![Результаты профиля][ImageProfileResults]  

<span data-ttu-id="50fd3-162">Wow, это является большим объемом данных.</span><span class="sxs-lookup"><span data-stu-id="50fd3-162">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="50fd3-163">Не беспокойтесь, это будет очень полезно в скором времени.</span><span class="sxs-lookup"><span data-stu-id="50fd3-163">Don't worry, it'll all make more sense shortly.</span></span>  

## <span data-ttu-id="50fd3-164">Анализ результатов</span><span class="sxs-lookup"><span data-stu-id="50fd3-164">Analyze the results</span></span>   

<span data-ttu-id="50fd3-165">После того как вы загрузили производительность страницы, вы можете оценить, насколько низкая производительность страницы, и найти причины.</span><span class="sxs-lookup"><span data-stu-id="50fd3-165">Once you've got a recording the performance of the page, you can measure how poor the performance of the page is, and find the any causes.</span></span>  

### <span data-ttu-id="50fd3-166">Анализ кадров в секунду</span><span class="sxs-lookup"><span data-stu-id="50fd3-166">Analyze frames per second</span></span>  

<span data-ttu-id="50fd3-167">Основная метрика для измерения производительности любой анимации — число кадров в секунду с повтором (кадр/с).</span><span class="sxs-lookup"><span data-stu-id="50fd3-167">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="50fd3-168">Пользователи будут рады, что анимации работают в 60 кадр/с.</span><span class="sxs-lookup"><span data-stu-id="50fd3-168">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="50fd3-169">Посмотрите на диаграмму в **кадре** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-169">Look at the **FPS** chart.</span></span>  <span data-ttu-id="50fd3-170">Если вы видите красную полосу над **кадром кадров**, это означает, что частота кадров, отброшенных таким образом, что она может повредить взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="50fd3-170">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="50fd3-171">Как правило, чем больше зеленая полоса, тем выше кадр кадров.</span><span class="sxs-lookup"><span data-stu-id="50fd3-171">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-172">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="50fd3-172">Figure 5</span></span>  
    > <span data-ttu-id="50fd3-173">Диаграмма кадр/с</span><span class="sxs-lookup"><span data-stu-id="50fd3-173">The FPS chart</span></span>  
    > ![Диаграмма кадр/с][ImageFPSChart]  

1.  <span data-ttu-id="50fd3-175">Под диаграммой с **кадром кадров** вы видите диаграмму **ЦП** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-175">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="50fd3-176">Цвета на диаграмме **ЦП** соответствуют цветам на вкладке " **Сводка** " в нижней части панели "производительность".</span><span class="sxs-lookup"><span data-stu-id="50fd3-176">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="50fd3-177">Тот факт, что диаграмма **ЦП** заполнена цветом, означает, что ЦП был maxed во время записи.</span><span class="sxs-lookup"><span data-stu-id="50fd3-177">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="50fd3-178">Всякий раз, когда вы видите maxed ЦП в течение длительного времени, это подсказка для поиска способов уменьшения объема работы.</span><span class="sxs-lookup"><span data-stu-id="50fd3-178">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-179">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="50fd3-179">Figure 6</span></span>  
    > <span data-ttu-id="50fd3-180">Вкладка "Диаграмма ЦП" и "Сводка"</span><span class="sxs-lookup"><span data-stu-id="50fd3-180">The CPU chart and Summary tab</span></span>  
    > ![Вкладка "Диаграмма ЦП" и "Сводка"][ImageCPUSummary]  

1.  <span data-ttu-id="50fd3-182">Наведите указатель мыши на диаграммы **кадров**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-182">Hover your mouse over the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="50fd3-183">В DevTools показан снимок страницы на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="50fd3-183">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="50fd3-184">Чтобы воспроизвести запись, передвиньте указатель влево и вправо.</span><span class="sxs-lookup"><span data-stu-id="50fd3-184">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="50fd3-185">Это называется чисткум, и его можно использовать для анализа хода анимации вручную.</span><span class="sxs-lookup"><span data-stu-id="50fd3-185">This is called scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-186">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="50fd3-186">Figure 7</span></span>  
    > <span data-ttu-id="50fd3-187">Просмотр снимка страницы в 2500ms отметке записи</span><span class="sxs-lookup"><span data-stu-id="50fd3-187">Viewing a screenshot of the page around the 2500ms mark of the recording</span></span>  
    > ![Просмотр снимка страницы в 2500ms отметке записи][ImageViewingScreenshot]  

1.  <span data-ttu-id="50fd3-189">В разделе **кадры** наведите указатель мыши на один из зеленых квадратиков.</span><span class="sxs-lookup"><span data-stu-id="50fd3-189">In the **Frames** section, hover your mouse over one of the green squares.</span></span>  <span data-ttu-id="50fd3-190">DevTools показывает, что этот конкретный кадр находится в кадре/сек.</span><span class="sxs-lookup"><span data-stu-id="50fd3-190">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="50fd3-191">Скорее всего, каждый кадр расположен ниже целевого числа 60 кадр/с.</span><span class="sxs-lookup"><span data-stu-id="50fd3-191">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-192">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="50fd3-192">Figure 8</span></span>  
    > <span data-ttu-id="50fd3-193">Наведение указателя мыши на рамку</span><span class="sxs-lookup"><span data-stu-id="50fd3-193">Hovering over a frame</span></span>  
    > ![Наведение указателя мыши на рамку][ImageFrameHover]  

<span data-ttu-id="50fd3-195">Разумеется, в этом ролике очень очевидно, что страница не работает хорошо.</span><span class="sxs-lookup"><span data-stu-id="50fd3-195">Of course, with this demo, it is pretty obvious that the page is not performing well.</span></span>  <span data-ttu-id="50fd3-196">Но в реальных сценариях это может быть не так, поэтому все эти средства помогут вам сделать измерения весьма удобными.</span><span class="sxs-lookup"><span data-stu-id="50fd3-196">But in real scenarios, it may not be so clear, so having all of these tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="50fd3-197">Премия: открытие индикатора кадров</span><span class="sxs-lookup"><span data-stu-id="50fd3-197">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="50fd3-198">Еще одним удобным инструментом является индикатор между КАДРами, который обеспечивает оценки в реальном времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="50fd3-198">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="50fd3-199">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="50fd3-199">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="50fd3-200">Начните вводить текст `Rendering` в меню команд и выберите пункт **Показать отрисовку**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-200">Start typing `Rendering` in the Command Menu and select **Show Rendering**.</span></span>  
1.  <span data-ttu-id="50fd3-201">На вкладке " **рендеринг** " Включите **индикатор кадров**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-201">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="50fd3-202">В правом верхнем углу окна просмотра появится новая наложение.</span><span class="sxs-lookup"><span data-stu-id="50fd3-202">A new overlay appears in the top-right of your viewport.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-203">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="50fd3-203">Figure 9</span></span>  
    > <span data-ttu-id="50fd3-204">Индикатор кадров в кадре</span><span class="sxs-lookup"><span data-stu-id="50fd3-204">The FPS meter</span></span>  
    > ![Индикатор кадров в кадре][ImageFPSMeter]  

1.  <span data-ttu-id="50fd3-206">Отключите **индикатор кадров** , а затем нажмите `Escape` , чтобы закрыть вкладку **рендеринг** .  Вы не будете использовать его в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="50fd3-206">Disable the **FPS Meter** and press `Escape` to close the **Rendering** tab.  You won't be using it in this tutorial.</span></span>  

### <span data-ttu-id="50fd3-207">Определение узкого места</span><span class="sxs-lookup"><span data-stu-id="50fd3-207">Find the bottleneck</span></span>  

<span data-ttu-id="50fd3-208">Теперь, когда вы проверили, что анимация не работает, следующий вопрос для ответа: почему?</span><span class="sxs-lookup"><span data-stu-id="50fd3-208">Now that you've measured and verified that the animation is not performing well, the next question to answer is:  why?</span></span>  

1.  <span data-ttu-id="50fd3-209">Обратите внимание на вкладку Сводка.  Если не выбрано ни одного события, на этой вкладке показана разбивка действий.</span><span class="sxs-lookup"><span data-stu-id="50fd3-209">Note the summary tab.  When no events are selected, this tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="50fd3-210">Страница потратила большую часть ее отображения времени.</span><span class="sxs-lookup"><span data-stu-id="50fd3-210">The page spent most of its time rendering.</span></span>  <span data-ttu-id="50fd3-211">Так как производительность — это изображение, которое уменьшает трудозатраты, цель состоит в том, чтобы уменьшить время, затраченное на обработку результатов.</span><span class="sxs-lookup"><span data-stu-id="50fd3-211">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-212">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="50fd3-212">Figure 10</span></span>  
    > <span data-ttu-id="50fd3-213">Вкладка "Сводка"</span><span class="sxs-lookup"><span data-stu-id="50fd3-213">The Summary tab</span></span>  
    > ![Вкладка "Сводка"][ImageSummaryTab]  

1.  <span data-ttu-id="50fd3-215">Разверните раздел **основной** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-215">Expand the **Main** section.</span></span>  <span data-ttu-id="50fd3-216">DevTools показывает flameную диаграмму активности в главном потоке с течением времени.</span><span class="sxs-lookup"><span data-stu-id="50fd3-216">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="50fd3-217">С течением времени ось x представляет запись.</span><span class="sxs-lookup"><span data-stu-id="50fd3-217">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="50fd3-218">Каждая строка представляет событие.</span><span class="sxs-lookup"><span data-stu-id="50fd3-218">Each bar represents an event.</span></span>  <span data-ttu-id="50fd3-219">Более широкий отрезок означает, что событие занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="50fd3-219">A wider bar means that event took longer.</span></span>  <span data-ttu-id="50fd3-220">Ось y представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="50fd3-220">The y-axis represents the call stack.</span></span>  <span data-ttu-id="50fd3-221">Если вы видите события, наложенные друг на друга, это означает, что события верхнего уровня приводили к появлению младших событий.</span><span class="sxs-lookup"><span data-stu-id="50fd3-221">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    > ##### <span data-ttu-id="50fd3-222">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="50fd3-222">Figure 11</span></span>  
    > <span data-ttu-id="50fd3-223">Основной раздел</span><span class="sxs-lookup"><span data-stu-id="50fd3-223">The Main section</span></span>  
    > ![Основной раздел][ImageMainSection]  

1.  <span data-ttu-id="50fd3-225">В записи много данных.</span><span class="sxs-lookup"><span data-stu-id="50fd3-225">There is a lot of data in the recording.</span></span>  <span data-ttu-id="50fd3-226">Увеличить одно событие можно, нажав и удерживая указатель мыши над **обзором**, который включает в себя раздел с диаграммами в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-226">Zoom in on a single event by clicking, holding, and dragging your mouse over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="50fd3-227">В **главном** разделе и на вкладке " **Сводка** " отображаются только сведения о выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="50fd3-227">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    > ###### <span data-ttu-id="50fd3-228">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="50fd3-228">Figure 12</span></span>  
    > <span data-ttu-id="50fd3-229">Увеличено на одном событии</span><span class="sxs-lookup"><span data-stu-id="50fd3-229">Zoomed in on a single event</span></span>  
    > ![Увеличено на событии][ImageZoomedAnimation]  
    
    > [!NOTE]
    > <span data-ttu-id="50fd3-231">Еще один способ увеличить масштаб — сосредоточиться на **основном** разделе, щелкнув его фон или выбрав событие, а затем нажать клавиши,, и, удерживая нажатой клавишу `W` `A` `S` `D` .</span><span class="sxs-lookup"><span data-stu-id="50fd3-231">Another way to zoom is to focus the **Main** section by clicking its background or selecting an event, and then press the `W`, `A`, `S`, and `D` keys.</span></span>  
    
    1.  <span data-ttu-id="50fd3-232">Обратите внимание на красный треугольник в правой верхней части события **анимации Frame, инициированной анимацией** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-232">Note the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="50fd3-233">Если вы видите красный треугольник, это предупреждение может быть связано с проблемой, связанной с этим событием.</span><span class="sxs-lookup"><span data-stu-id="50fd3-233">Whenever you see a red triangle, it is a warning that there may be an issue related to this event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="50fd3-234">Событие **анимации Frame срабатывает** при каждом запуске [ `requestAnimationFrame()` обратного вызова][MDNWebRequestAnimationFrame] .</span><span class="sxs-lookup"><span data-stu-id="50fd3-234">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="50fd3-235">Щелкните событие **кадр анимации, которое активировалось** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-235">Click the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="50fd3-236">На вкладке **Сводка** теперь отображаются сведения об этом событии.</span><span class="sxs-lookup"><span data-stu-id="50fd3-236">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="50fd3-237">Обратите внимание на ссылку " **Показать** ".</span><span class="sxs-lookup"><span data-stu-id="50fd3-237">Note the **Reveal** link.</span></span>  <span data-ttu-id="50fd3-238">Щелчок приводит к тому, что DevTools выделит событие, которое инициировало событие Frame, инициированной **анимацией** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-238">Clicking that causes DevTools to highlight the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="50fd3-239">Также обратите внимание на ссылку **app. js: 95** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-239">Also note the **app.js:95** link.</span></span>  <span data-ttu-id="50fd3-240">При нажатии этой кнопки осуществляется переход к нужной строке исходного кода.</span><span class="sxs-lookup"><span data-stu-id="50fd3-240">Clicking that jumps you to the relevant line in the source code.</span></span>
    
    > ##### <span data-ttu-id="50fd3-241">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="50fd3-241">Figure 13</span></span>  
    > <span data-ttu-id="50fd3-242">Дополнительные сведения о событии анимации запускаемого кадра</span><span class="sxs-lookup"><span data-stu-id="50fd3-242">More information about the Animation Frame Fired event</span></span>  
    > ![Дополнительные сведения о событии анимации запускаемого кадра][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > <span data-ttu-id="50fd3-244">После выбора события с помощью клавиш со стрелками выберите события рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="50fd3-244">After selecting an event, use the arrow keys to select the events next to it.</span></span>  

1.  <span data-ttu-id="50fd3-245">В рамках события **app. Update** существует множество фиолетовых событий.</span><span class="sxs-lookup"><span data-stu-id="50fd3-245">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="50fd3-246">Если бы они были шире, они будут выглядеть так, как будто для каждого из них имеется красный треугольник.</span><span class="sxs-lookup"><span data-stu-id="50fd3-246">If they were wider, it looks as though each one might have a red triangle on it.</span></span>  <span data-ttu-id="50fd3-247">Щелкните одно из фиолетовых событий **макета** .</span><span class="sxs-lookup"><span data-stu-id="50fd3-247">Click one of the purple **Layout** events now.</span></span>  <span data-ttu-id="50fd3-248">DevTools предоставляет дополнительные сведения о событии на вкладке " **Сводка** ".  В действительности есть предупреждение о принудительном передвижении \ (другое слово для макета \).</span><span class="sxs-lookup"><span data-stu-id="50fd3-248">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  

1.  <span data-ttu-id="50fd3-249">На вкладке **Сводка** щелкните ссылку **app. js: 71** в разделе **Макет принудительно**.</span><span class="sxs-lookup"><span data-stu-id="50fd3-249">In the **Summary** tab, click the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="50fd3-250">DevTools перенесет вас в строку кода, которая замещает макет.</span><span class="sxs-lookup"><span data-stu-id="50fd3-250">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    > ##### <span data-ttu-id="50fd3-251">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="50fd3-251">Figure 14</span></span>  
    > <span data-ttu-id="50fd3-252">Строка кода, вызвавшая принудительный макет.</span><span class="sxs-lookup"><span data-stu-id="50fd3-252">The line of code that caused the forced layout</span></span>  
    > ![Строка кода, вызвавшая принудительный макет.][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > <span data-ttu-id="50fd3-254">Проблема с этим кодом состоит в том, что в каждом кадре анимации меняется стиль каждого значка, а затем запрашивается расположение каждого значка на странице.</span><span class="sxs-lookup"><span data-stu-id="50fd3-254">The problem with this code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="50fd3-255">Поскольку стили изменились, браузер не знает о том, изменилось ли положение каждого значка, поэтому для вычисления его положения необходимо изменить макет значка.</span><span class="sxs-lookup"><span data-stu-id="50fd3-255">Because the styles changed, the browser doesn't know if each icon position changed, so it has to re-layout the icon in order to compute its position.</span></span>  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

<span data-ttu-id="50fd3-256">Phew!</span><span class="sxs-lookup"><span data-stu-id="50fd3-256">Phew!</span></span>  <span data-ttu-id="50fd3-257">Это было бы очень много, но теперь у вас есть надежная основа базового рабочего процесса для анализа производительности среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="50fd3-257">That was a lot to take in, but you now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="50fd3-258">Молодец.</span><span class="sxs-lookup"><span data-stu-id="50fd3-258">Good job.</span></span>  

### <span data-ttu-id="50fd3-259">Премия: анализ оптимизированной версии</span><span class="sxs-lookup"><span data-stu-id="50fd3-259">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="50fd3-260">Используй рабочие процессы и инструменты, которые вы только что узнали, нажмите кнопку **оптимизировать** на демонстрационной версии, чтобы включить оптимизированный код, переведите другую запись и проанализируйте результаты.</span><span class="sxs-lookup"><span data-stu-id="50fd3-260">Using the workflows and tools that you just learned, click **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="50fd3-261">С улучшенной частотой кадров, направленной на сокращение событий в диаграмме Flame в **главном** разделе, можно увидеть, что оптимизированная версия приложения работает гораздо меньше, что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="50fd3-261">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you can see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="50fd3-262">Несмотря на то, что эта "оптимизированная" версия не подходит, так как она по-прежнему обрабатывает `top` свойство каждого значка.</span><span class="sxs-lookup"><span data-stu-id="50fd3-262">Even this "optimized" version isn't that great, because it still manipulates the `top` property of each icon.</span></span>  <span data-ttu-id="50fd3-263">Лучший подход — придерживаться свойств, которые влияют только на композицию.</span><span class="sxs-lookup"><span data-stu-id="50fd3-263">A better approach is to stick to properties that only affect compositing.</span></span>  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="50fd3-264">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="50fd3-264">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="50fd3-265">Для более удобного функционирования с помощью панели "производительность" лучше всего сделать это.</span><span class="sxs-lookup"><span data-stu-id="50fd3-265">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="50fd3-266">Попробуйте выполнить профилирование на своих страницах и проанализировать результаты.</span><span class="sxs-lookup"><span data-stu-id="50fd3-266">Try profiling your own pages and analyzing the results.</span></span>  <span data-ttu-id="50fd3-267">Если у вас возникли вопросы по поводу ваших результатов, используйте значок **обратной связи** , нажмите `Alt`  +  `Shift`  +  `I` на Windows ( `Option`  +  `Shift`  +  `I` на macOS) или [твит][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="50fd3-267">If you have any questions about your results, use the **Feedback** icon, press `Alt` + `Shift` + `I` on Windows (`Option` + `Shift` + `I` on macOS), or [tweet at us][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="50fd3-268">Включите снимки экрана или ссылки на воспроизводимые страницы, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="50fd3-268">Include screenshots or links to reproducible pages, if possible.</span></span>

> ##### <span data-ttu-id="50fd3-269">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="50fd3-269">Figure 15</span></span>
> <span data-ttu-id="50fd3-270">Значок **обратной связи** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="50fd3-270">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![Значок \* \* Feedback \* \* в Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="50fd3-272">Наконец, существует множество способов улучшить производительность во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="50fd3-272">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="50fd3-273">В этом учебнике рассмотрены определенные узкие места анимации, направленные на экран с помощью панели производительности, но это только одно из многих узких мест.</span><span class="sxs-lookup"><span data-stu-id="50fd3-273">This tutorial focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Рисунок 1: демонстрация слева и DevTools справа"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Рисунок 2: регулирование центрального процессора"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Рисунок 3: Профилирование страницы"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Рисунок 4: результаты работы с профилем"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Рисунок 5: диаграмма кадр/с"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Рисунок 6: вкладка "Диаграмма ЦП" и "Сводка", выделенная синим цветом"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Рисунок 7: Просмотр снимка страницы в 2500ms отметке записи"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Рисунок 8: наведение указателя мыши на кадр"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Рисунок 9: индикатор кадров в кадре"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Рисунок 10: вкладка "Сводка""  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "На рисунке 11: основной раздел"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Рисунок 12: масштабирование одной анимации кадром, вызванным событием"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Рисунок 13. Дополнительные сведения о событии анимации Frame активировалось"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Рисунок 14: строка кода, вызвавшая принудительный макет."  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Рисунок 15: значок * * Feedback * * в Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-опубликовать твит | Контента"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="50fd3-293">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50fd3-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="50fd3-294">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="50fd3-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="50fd3-296">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50fd3-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

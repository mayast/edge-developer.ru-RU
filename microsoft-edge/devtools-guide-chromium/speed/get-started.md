---
title: Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 7efc76fbcb3d1ed6cbd0760f789c8c952030d70c
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611891"
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





# <span data-ttu-id="5d958-103">Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5d958-103">Optimize Website Speed With Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="5d958-104">Цель учебника</span><span class="sxs-lookup"><span data-stu-id="5d958-104">Goal of tutorial</span></span>  

<span data-ttu-id="5d958-105">В этом учебнике объясняется, как использовать Microsoft Edge DevTools, чтобы найти способы быстрой загрузки веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="5d958-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="5d958-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5d958-106">Prerequisites</span></span>  

*   <span data-ttu-id="5d958-107">У вас должен быть базовый интерфейс разработки веб-приложений, аналогично тому, что научились в этом [Знакомство с классом веб-разработки][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="5d958-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="5d958-108">Вам ничего не нужно знать о быстродействии нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5d958-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="5d958-109">В этом учебнике вы узнаете об этом.</span><span class="sxs-lookup"><span data-stu-id="5d958-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="5d958-110">Введение</span><span class="sxs-lookup"><span data-stu-id="5d958-110">Introduction</span></span>   

<span data-ttu-id="5d958-111">Это Илья.</span><span class="sxs-lookup"><span data-stu-id="5d958-111">This is Tony.</span></span>  <span data-ttu-id="5d958-112">Илья чрезвычайно знаменита в отношении Cat общества.</span><span class="sxs-lookup"><span data-stu-id="5d958-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="5d958-113">Он создал веб-сайт, чтобы его вентиляторы могли узнать о своем любимом продуктов.</span><span class="sxs-lookup"><span data-stu-id="5d958-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="5d958-114">Его вентиляторы понравятся на сайте, но в Илья сохраняются жалобы, которые медленно загружаются на сайт.</span><span class="sxs-lookup"><span data-stu-id="5d958-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="5d958-115">Илья предложит вам помочь ему ускорить работу сайта.</span><span class="sxs-lookup"><span data-stu-id="5d958-115">Tony has asked you to help him speed the site up.</span></span>  

> ##### <span data-ttu-id="5d958-116">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="5d958-116">Figure 1</span></span>  
> <span data-ttu-id="5d958-117">Илья CAT</span><span class="sxs-lookup"><span data-stu-id="5d958-117">Tony the cat</span></span>  
> ![Илья CAT][ImageTony]  

## <span data-ttu-id="5d958-119">Действие 1: аудит сайта</span><span class="sxs-lookup"><span data-stu-id="5d958-119">Step 1: Audit the site</span></span>   

<span data-ttu-id="5d958-120">Всякий раз, когда вы захотите улучшить производительность загрузки сайта, **всегда начинайте с аудита**.</span><span class="sxs-lookup"><span data-stu-id="5d958-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="5d958-121">Аудитория имеет 2 важные функции.</span><span class="sxs-lookup"><span data-stu-id="5d958-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="5d958-122">Она создает **базовый план** для измерения последующих изменений.</span><span class="sxs-lookup"><span data-stu-id="5d958-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="5d958-123">Здесь вы найдете **Советы** , которые помогут вам изменить наиболее благоприятные изменения.</span><span class="sxs-lookup"><span data-stu-id="5d958-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  

### <span data-ttu-id="5d958-124">Настройка</span><span class="sxs-lookup"><span data-stu-id="5d958-124">Set up</span></span>   

<span data-ttu-id="5d958-125">Сначала необходимо настроить сайт, чтобы вы могли вносить в него изменения позже.</span><span class="sxs-lookup"><span data-stu-id="5d958-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="5d958-126">[Откройте исходный код для сайта](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="5d958-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="5d958-127">Эта вкладка называется **вкладкой "редактор"**.</span><span class="sxs-lookup"><span data-stu-id="5d958-127">This tab is referred to as the **editor tab**.</span></span>  
    
    > ##### <span data-ttu-id="5d958-128">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="5d958-128">Figure 2</span></span>  
    > <span data-ttu-id="5d958-129">Вкладка "редактор"</span><span class="sxs-lookup"><span data-stu-id="5d958-129">The editor tab</span></span>  
    > ![Вкладка "редактор"][ImageEditor]  

1.  <span data-ttu-id="5d958-131">Выберите **Илья**.</span><span class="sxs-lookup"><span data-stu-id="5d958-131">Select **tony**.</span></span>  <span data-ttu-id="5d958-132">Откроется меню.</span><span class="sxs-lookup"><span data-stu-id="5d958-132">A menu appears.</span></span>  
    
    > ##### <span data-ttu-id="5d958-133">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="5d958-133">Figure 3</span></span>  
    > <span data-ttu-id="5d958-134">Меню, которое появляется после нажатия кнопки **Илья**</span><span class="sxs-lookup"><span data-stu-id="5d958-134">The menu that appears after clicking **tony**</span></span>  
    > ![Меню, которое появляется после нажатия кнопки Илья][ImageMenu]  
    
1.  <span data-ttu-id="5d958-136">Выберите **Remix проект**.</span><span class="sxs-lookup"><span data-stu-id="5d958-136">Select **Remix Project**.</span></span>  <span data-ttu-id="5d958-137">Имя проекта меняется с **Илья** на случайное сгенерированное имя.</span><span class="sxs-lookup"><span data-stu-id="5d958-137">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="5d958-138">Теперь у вас есть Редактируемая копия кода.</span><span class="sxs-lookup"><span data-stu-id="5d958-138">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="5d958-139">Позже вы можете внести изменения в этот код.</span><span class="sxs-lookup"><span data-stu-id="5d958-139">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="5d958-140">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="5d958-140">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="5d958-141">Демонстрационный ролик откроется на новой вкладке.  Эта вкладка упоминается как **вкладка Demo**.  Загрузка сайта может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="5d958-141">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    > ##### <span data-ttu-id="5d958-142">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="5d958-142">Figure 4</span></span>  
    > <span data-ttu-id="5d958-143">Вкладка "демонстрация"</span><span class="sxs-lookup"><span data-stu-id="5d958-143">The demo tab</span></span>  
    > ![Вкладка "демонстрация"][ImageDemo]  

1.  <span data-ttu-id="5d958-145">Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="5d958-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="5d958-146">Рядом с демоном DevTools откроется Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d958-146">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    > ##### <span data-ttu-id="5d958-147">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="5d958-147">Figure 5</span></span>  
    > <span data-ttu-id="5d958-148">DevTools и демонстрация</span><span class="sxs-lookup"><span data-stu-id="5d958-148">DevTools and the demo</span></span>  
    > ![DevTools и демонстрация][ImageDevtools]  

<span data-ttu-id="5d958-150">Для остальных снимков экрана в этом учебнике DevTools отображается в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="5d958-150">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="5d958-151">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите его `Undock` и выберите команду **открепить в отдельном окне**.</span><span class="sxs-lookup"><span data-stu-id="5d958-151">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

> ##### <span data-ttu-id="5d958-152">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="5d958-152">Figure 6</span></span>  
> <span data-ttu-id="5d958-153">Незакрепленные DevTools</span><span class="sxs-lookup"><span data-stu-id="5d958-153">Undocked DevTools</span></span>  
> ![Незакрепленные DevTools][ImageUndocked]  

### <span data-ttu-id="5d958-155">Создание базового плана</span><span class="sxs-lookup"><span data-stu-id="5d958-155">Establish a baseline</span></span>   

<span data-ttu-id="5d958-156">Базовый план — это запись того, как выполняется сайт, прежде чем вы внесли улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="5d958-156">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="5d958-157">Перейдите на вкладку **Аудит** .  Он может быть скрыт за кнопкой **Дополнительные панели** ![ ][ImageMorePanelsIcon] .</span><span class="sxs-lookup"><span data-stu-id="5d958-157">Select the **Audits** tab.  It may be hidden behind the **More Panels** ![More Panels][ImageMorePanelsIcon] button.</span></span>  <span data-ttu-id="5d958-158">На этой панели есть Lighthouse, так как проект, который включает панель «аудиты», называется **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="5d958-158">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    > ##### <span data-ttu-id="5d958-159">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="5d958-159">Figure 7</span></span>  
    > <span data-ttu-id="5d958-160">Панель «аудит»</span><span class="sxs-lookup"><span data-stu-id="5d958-160">The Audits panel</span></span>  
    > ![Панель «аудит»][ImageAudits]  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="5d958-162">В соответствии с параметрами настройки аудита на [рисунке 7](#figure-7).</span><span class="sxs-lookup"><span data-stu-id="5d958-162">Match your audit configuration settings to those in [Figure 7](#figure-7).</span></span>  <span data-ttu-id="5d958-163">Ниже приведено описание различных параметров.</span><span class="sxs-lookup"><span data-stu-id="5d958-163">Here is an explanation of the different options:</span></span>  

    *   <span data-ttu-id="5d958-164">**Устройства**.</span><span class="sxs-lookup"><span data-stu-id="5d958-164">**Device**.</span></span>  <span data-ttu-id="5d958-165">При настройке на **мобильном устройстве** изменяется строка агента пользователя и имитируется мобильное окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="5d958-165">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="5d958-166">Настройка для **настольного компьютера** очень просто отключает изменения на **мобильном устройстве** .</span><span class="sxs-lookup"><span data-stu-id="5d958-166">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="5d958-167">**Аудита**.</span><span class="sxs-lookup"><span data-stu-id="5d958-167">**Audits**.</span></span>  <span data-ttu-id="5d958-168">Отключение категории не позволяет панели аудита выполнять эти проверки и исключает из отчета эти проверки.</span><span class="sxs-lookup"><span data-stu-id="5d958-168">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="5d958-169">Если вы хотите просмотреть предоставленные типы рекомендаций, оставьте другие доступные категории.</span><span class="sxs-lookup"><span data-stu-id="5d958-169">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="5d958-170">Отключение категорий немного ускоряет процесс аудита.</span><span class="sxs-lookup"><span data-stu-id="5d958-170">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="5d958-171">**Регулирование**.</span><span class="sxs-lookup"><span data-stu-id="5d958-171">**Throttling**.</span></span>  <span data-ttu-id="5d958-172">Для **эмуляции медленного 4G, скорость процессора 4X** эмулирует типичные условия обзора на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="5d958-172">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="5d958-173">Она называется смоделированной, так как панель "Аудит" не выполняет никаких действий по регулированию в процессе аудита.</span><span class="sxs-lookup"><span data-stu-id="5d958-173">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="5d958-174">Вместо этого оно просто экстраполяция того, сколько времени займет загрузка страницы в условиях мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5d958-174">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="5d958-175">Параметр " **применено...** ", в свою очередь, в действительности регулирует производительность процессора и сети с компромиссом более продолжительного процесса аудита.</span><span class="sxs-lookup"><span data-stu-id="5d958-175">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="5d958-176">**Очистите хранилище**.</span><span class="sxs-lookup"><span data-stu-id="5d958-176">**Clear Storage**.</span></span>  <span data-ttu-id="5d958-177">При установке этого флажка все хранилище, связанное со страницей, будет очищено перед каждым аудитом.</span><span class="sxs-lookup"><span data-stu-id="5d958-177">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="5d958-178">Оставьте этот параметр, если вы хотите подвергать аудиту, как посетители в первый раз будут работать на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="5d958-178">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="5d958-179">Отключите этот параметр, если вы хотите использовать функцию повторного посещения.</span><span class="sxs-lookup"><span data-stu-id="5d958-179">Disable this setting when you want the repeat-visit experience.</span></span>  

1.  <span data-ttu-id="5d958-180">Нажмите кнопку **запустить аудиты**.</span><span class="sxs-lookup"><span data-stu-id="5d958-180">Select **Run Audits**.</span></span>  <span data-ttu-id="5d958-181">После 10 – 30 секунд на панели «аудиты» отображается отчет о быстродействии сайта.</span><span class="sxs-lookup"><span data-stu-id="5d958-181">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    > ##### <span data-ttu-id="5d958-182">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="5d958-182">Figure 8</span></span>  
    > <span data-ttu-id="5d958-183">Отчет для панели «аудит» для производительности сайта</span><span class="sxs-lookup"><span data-stu-id="5d958-183">The report for the Audits panel of the performance of the site</span></span>  
    > ![Отчет для панели «аудит» для производительности сайта][ImageReport]  

#### <span data-ttu-id="5d958-185">Обработка ошибок отчета</span><span class="sxs-lookup"><span data-stu-id="5d958-185">Handling report errors</span></span>   

<span data-ttu-id="5d958-186">Если вы когда-либо получаете сообщение об ошибке в отчете на панели аудиты, попробуйте запустить вкладку Demo из окна **InPrivate** без открытия других вкладок.</span><span class="sxs-lookup"><span data-stu-id="5d958-186">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="5d958-187">Это гарантирует, что вы используете Microsoft Edge из чистого состояния.</span><span class="sxs-lookup"><span data-stu-id="5d958-187">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="5d958-188">Определенные расширения Microsoft Edge часто мешают процессу аудита.</span><span class="sxs-lookup"><span data-stu-id="5d958-188">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
> ##### old Figure 9  
> A report that errored  
> ![A report that errored][ImageError]  
-->  

### <span data-ttu-id="5d958-189">Понимание отчета</span><span class="sxs-lookup"><span data-stu-id="5d958-189">Understand your report</span></span>   

<span data-ttu-id="5d958-190">Число в верхней части отчета является общим показателем эффективности сайта.</span><span class="sxs-lookup"><span data-stu-id="5d958-190">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="5d958-191">После внесения изменений в код вы должны увидеть этот номер.</span><span class="sxs-lookup"><span data-stu-id="5d958-191">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="5d958-192">Более высокие баллы означают более высокую производительность.</span><span class="sxs-lookup"><span data-stu-id="5d958-192">A higher score means better performance.</span></span>  

> ##### <span data-ttu-id="5d958-193">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="5d958-193">Figure 9</span></span>  
> <span data-ttu-id="5d958-194">Общая оценка производительности</span><span class="sxs-lookup"><span data-stu-id="5d958-194">The overall performance score</span></span>  
> <span data-ttu-id="5d958-195">! [Общая оценка производительности] [ImageOverall]</span><span class="sxs-lookup"><span data-stu-id="5d958-195">![The overall performance score][ImageOverall]</span></span>  

<span data-ttu-id="5d958-196">Раздел **метрики** содержит количественные измерения производительности сайта.</span><span class="sxs-lookup"><span data-stu-id="5d958-196">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="5d958-197">Каждая метрика обеспечивает различные аспекты производительности.</span><span class="sxs-lookup"><span data-stu-id="5d958-197">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="5d958-198">Например, при первом обобщении с **содержимым** появляется сообщение о том, что содержимое сначала закрашено на экран, что является важной вехой в восприятии загрузки страницы, в то время как в **интерактивном режиме** отмечается тот момент, когда страница будет готова для обработки взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="5d958-198">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

> ##### <span data-ttu-id="5d958-199">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="5d958-199">Figure 10</span></span>  
> <span data-ttu-id="5d958-200">Раздел метрики</span><span class="sxs-lookup"><span data-stu-id="5d958-200">The Metrics section</span></span>  
> <span data-ttu-id="5d958-201">! [Раздел метрик] [ImageMetrics]</span><span class="sxs-lookup"><span data-stu-id="5d958-201">![The Metrics section][ImageMetrics]</span></span>  

<span data-ttu-id="5d958-202">Щелкните выделенный выключатель на [рисунке 11](#figure-11) , чтобы просмотреть описание каждой метрики, а затем нажмите Дополнительные **сведения** , чтобы прочитать его документацию.</span><span class="sxs-lookup"><span data-stu-id="5d958-202">Select the highlighted toggle button in [Figure 11](#figure-11) to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

> ##### <span data-ttu-id="5d958-203">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="5d958-203">Figure 11</span></span>  
> <span data-ttu-id="5d958-204">Щелкните выделенный выключатель, чтобы развернуть элементы **метрик**</span><span class="sxs-lookup"><span data-stu-id="5d958-204">Select the highlighted toggle button to expand the **Metrics** items</span></span>  
> <span data-ttu-id="5d958-205">! [Щелкните выделенный выключатель, чтобы развернуть элементы метрик] [ImageFirstMeaningfulPaint]</span><span class="sxs-lookup"><span data-stu-id="5d958-205">![Select the highlighted toggle button to expand the Metrics items][ImageFirstMeaningfulPaint]</span></span>  

<span data-ttu-id="5d958-206">Под метриками представлен набор снимков экрана, показывающий, как страница выглядит как загруженная.</span><span class="sxs-lookup"><span data-stu-id="5d958-206">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

> ##### <span data-ttu-id="5d958-207">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="5d958-207">Figure 12</span></span>  
> <span data-ttu-id="5d958-208">Снимки экрана, посвященные загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="5d958-208">Screenshots of how the page looked while loading</span></span>  
> <span data-ttu-id="5d958-209">! [Снимки экрана, при загрузке которого выглядела страница] [ImageScreenshots]</span><span class="sxs-lookup"><span data-stu-id="5d958-209">![Screenshots of how the page looked while loading][ImageScreenshots]</span></span>  

<span data-ttu-id="5d958-210">В разделе " **возможности** " представлены конкретные советы по повышению производительности загрузки данной страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-210">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

> ##### <span data-ttu-id="5d958-211">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="5d958-211">Figure 13</span></span>  
> <span data-ttu-id="5d958-212">Раздел "возможности"</span><span class="sxs-lookup"><span data-stu-id="5d958-212">The Opportunities section</span></span>  
> <span data-ttu-id="5d958-213">! [Раздел возможностей] [ImageOpportunities]</span><span class="sxs-lookup"><span data-stu-id="5d958-213">![The Opportunities section][ImageOpportunities]</span></span>  

<span data-ttu-id="5d958-214">Выберите возможность, чтобы узнать больше о ней.</span><span class="sxs-lookup"><span data-stu-id="5d958-214">Select an opportunity to learn more about it.</span></span>  

> ##### <span data-ttu-id="5d958-215">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="5d958-215">Figure 14</span></span>  
> <span data-ttu-id="5d958-216">**Исключение ресурсов блокировки рендеринга** возможная сделка</span><span class="sxs-lookup"><span data-stu-id="5d958-216">**Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="5d958-217">! [Устранить ресурсы, блокирующие рендеринг, возможная сделка] [ImageCompression]</span><span class="sxs-lookup"><span data-stu-id="5d958-217">![Eliminate render-blocking resources opportunity][ImageCompression]</span></span>  

<span data-ttu-id="5d958-218">Выберите дополнительные **сведения** , чтобы ознакомиться с документацией о важности возможной сделки, и конкретные рекомендации по ее устранению.</span><span class="sxs-lookup"><span data-stu-id="5d958-218">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

> ##### <span data-ttu-id="5d958-219">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="5d958-219">Figure 15</span></span>  
> <span data-ttu-id="5d958-220">Документация по **устранению ресурсов с блокировкой рендеринга** возможная сделка</span><span class="sxs-lookup"><span data-stu-id="5d958-220">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="5d958-221">! [Документация по устранению ресурсов, блокирующих обработку. Возможная сделка] [ImageReference]</span><span class="sxs-lookup"><span data-stu-id="5d958-221">![Documentation for the Eliminate render-blocking resources opportunity][ImageReference]</span></span>  

<span data-ttu-id="5d958-222">Раздел **Диагностика** содержит дополнительные сведения о факторах, которые влияют на время загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-222">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

> ##### <span data-ttu-id="5d958-223">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="5d958-223">Figure 16</span></span>  
> <span data-ttu-id="5d958-224">Раздел "Диагностика"</span><span class="sxs-lookup"><span data-stu-id="5d958-224">The Diagnostics section</span></span>  
> <span data-ttu-id="5d958-225">! [Раздел диагностика] [ImageDiagnostics]</span><span class="sxs-lookup"><span data-stu-id="5d958-225">![The Diagnostics section][ImageDiagnostics]</span></span>  

<span data-ttu-id="5d958-226">В разделе **переданные аудиты** показано, что делает сайт правильно.</span><span class="sxs-lookup"><span data-stu-id="5d958-226">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="5d958-227">Выберите этот пункт, чтобы развернуть раздел.</span><span class="sxs-lookup"><span data-stu-id="5d958-227">Select to expand the section.</span></span>  

> ##### <span data-ttu-id="5d958-228">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="5d958-228">Figure 17</span></span>  
> <span data-ttu-id="5d958-229">Раздел "пройденные аудиты"</span><span class="sxs-lookup"><span data-stu-id="5d958-229">The Passed Audits section</span></span>  
> <span data-ttu-id="5d958-230">! [Переданный раздел аудита] [ImagePassed]</span><span class="sxs-lookup"><span data-stu-id="5d958-230">![The Passed Audits section][ImagePassed]</span></span>  

## <span data-ttu-id="5d958-231">Этап 2: эксперименты</span><span class="sxs-lookup"><span data-stu-id="5d958-231">Step 2: Experiment</span></span>   

<span data-ttu-id="5d958-232">Раздел "возможности" в отчете об аудите содержит советы по улучшению производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-232">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="5d958-233">В этом разделе вы реализуете рекомендованные изменения в базе кода, проведя аудит сайта после каждого изменения, чтобы определить, как оно влияет на скорость сайта.</span><span class="sxs-lookup"><span data-stu-id="5d958-233">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="5d958-234">Включение сжатия текста</span><span class="sxs-lookup"><span data-stu-id="5d958-234">Enable text compression</span></span>   

<span data-ttu-id="5d958-235">В отчете говорится, что отсутствие огромных полезных данных сети является одной из самых первых возможностей для повышения производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-235">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="5d958-236">Включить сжатие текста — это возможность улучшить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-236">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="5d958-237">Сжатие текста — это сокращение размера текстового файла перед отправкой по сети, а также его сжатие.</span><span class="sxs-lookup"><span data-stu-id="5d958-237">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="5d958-238">Например, вы можете почтовые индексы, чтобы уменьшить размер папки.</span><span class="sxs-lookup"><span data-stu-id="5d958-238">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="5d958-239">Перед включением сжатия вы можете вручную проверить, сжимаются ли текстовые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5d958-239">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="5d958-240">Откройте вкладку **сеть** .</span><span class="sxs-lookup"><span data-stu-id="5d958-240">Select the **Network** tab.</span></span>  
    
    > ##### <span data-ttu-id="5d958-241">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="5d958-241">Figure 18</span></span>  
    > <span data-ttu-id="5d958-242">Панель "сеть"</span><span class="sxs-lookup"><span data-stu-id="5d958-242">The Network panel</span></span>  
    > <span data-ttu-id="5d958-243">! [Панель сети] [ImageNetwork]</span><span class="sxs-lookup"><span data-stu-id="5d958-243">![The Network panel][ImageNetwork]</span></span>  
    
1.  <span data-ttu-id="5d958-244">Выберите значок **Параметры сети** .</span><span class="sxs-lookup"><span data-stu-id="5d958-244">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="5d958-245">Установите флажок **использовать строки большого запроса** .</span><span class="sxs-lookup"><span data-stu-id="5d958-245">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="5d958-246">Высота строк в таблице сетевых запросов возрастает.</span><span class="sxs-lookup"><span data-stu-id="5d958-246">The height of the rows in the table of network requests increases.</span></span>  
    
    > ##### <span data-ttu-id="5d958-247">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="5d958-247">Figure 19</span></span>  
    > <span data-ttu-id="5d958-248">Большие строки в таблице "сетевые запросы"</span><span class="sxs-lookup"><span data-stu-id="5d958-248">Large rows in the network requests table</span></span>  
    > <span data-ttu-id="5d958-249">! [Большие строки в таблице "сетевые запросы"] [ImageLargeRows]</span><span class="sxs-lookup"><span data-stu-id="5d958-249">![Large rows in the network requests table][ImageLargeRows]</span></span>  
    
1.  <span data-ttu-id="5d958-250">Если столбец **Размер** не отображается в таблице сетевых запросов, щелкните заголовок таблицы и выберите команду **Размер**.</span><span class="sxs-lookup"><span data-stu-id="5d958-250">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="5d958-251">В каждой ячейке **размера** отображаются два значения.</span><span class="sxs-lookup"><span data-stu-id="5d958-251">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="5d958-252">Верхнее значение — размер загруженного ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d958-252">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="5d958-253">Минимальное значение — размер несжатого ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d958-253">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="5d958-254">Если оба значения совпадают, значит, ресурс не сжимается, когда он отправляется по сети.</span><span class="sxs-lookup"><span data-stu-id="5d958-254">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="5d958-255">Например, на [рисунке 19](#figure-19) значения Top и Bottom для "" `bundle.js` — " `1.2 MB` и" `1.2 MB` ... ".</span><span class="sxs-lookup"><span data-stu-id="5d958-255">For example, in [Figure 19](#figure-19) the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="5d958-256">Проверка на наличие сжатия с помощью проверки заголовков HTTP ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d958-256">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="5d958-257">Выберите **пакет. js**.</span><span class="sxs-lookup"><span data-stu-id="5d958-257">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="5d958-258">Откройте вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="5d958-258">Select the **Headers** tab.</span></span>  
    
    > ##### <span data-ttu-id="5d958-259">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="5d958-259">Figure 20</span></span>  
    > <span data-ttu-id="5d958-260">Вкладка "заголовки"</span><span class="sxs-lookup"><span data-stu-id="5d958-260">The Headers tab</span></span>  
    > <span data-ttu-id="5d958-261">! [Вкладка Заголовки] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="5d958-261">![The Headers tab][ImageHeaders]</span></span>  
    
1.  <span data-ttu-id="5d958-262">Поиск заголовка в разделе **заголовков ответа** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="5d958-262">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="5d958-263">Вы не видите один из них, то есть `bundle.js` не был сжат.</span><span class="sxs-lookup"><span data-stu-id="5d958-263">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="5d958-264">Когда ресурс сжимается, этот верхний колонтитул обычно имеет значение `gzip` , `deflate` или `br` .</span><span class="sxs-lookup"><span data-stu-id="5d958-264">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="5d958-265">Описание этих значений показано в разделе [директивы][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="5d958-265">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="5d958-266">Достаточно с пояснениями.</span><span class="sxs-lookup"><span data-stu-id="5d958-266">Enough with the explanations.</span></span>  <span data-ttu-id="5d958-267">Время, чтобы внести некоторые изменения!</span><span class="sxs-lookup"><span data-stu-id="5d958-267">Time to make some changes!</span></span>  <span data-ttu-id="5d958-268">Включите сжатие текста, добавив несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="5d958-268">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="5d958-269">На вкладке "редактор" щелкните **Server. js**.</span><span class="sxs-lookup"><span data-stu-id="5d958-269">In the editor tab, click **server.js**.</span></span>  
    
    > ##### <span data-ttu-id="5d958-270">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="5d958-270">Figure 21</span></span>  
    > <span data-ttu-id="5d958-271">Редактирование сервера. js</span><span class="sxs-lookup"><span data-stu-id="5d958-271">Editing server.js</span></span>  
    > <span data-ttu-id="5d958-272">! [Редактирование Server. js] [ImageServer]</span><span class="sxs-lookup"><span data-stu-id="5d958-272">![Editing server.js][ImageServer]</span></span>  
    
1.  <span data-ttu-id="5d958-273">Добавьте следующий код в **сервер Server. js**.</span><span class="sxs-lookup"><span data-stu-id="5d958-273">Add the following code to **server.js**.</span></span>  <span data-ttu-id="5d958-274">Убедитесь, что он должен быть помещен `app.use(compression())` `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="5d958-274">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="5d958-275">Как правило, вы должны установить `compression` пакет с помощью какого-либо вида `npm i -S compression` , но это еще не сделано.</span><span class="sxs-lookup"><span data-stu-id="5d958-275">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="5d958-276">Дождитесь, пока не будет развернуто новая сборка сайта.</span><span class="sxs-lookup"><span data-stu-id="5d958-276">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="5d958-277">Неузорная анимация рядом с **инструментами** означает, что сайт перестраивается и повторно развертывается.</span><span class="sxs-lookup"><span data-stu-id="5d958-277">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="5d958-278">Изменение будет готово, когда анимация рядом с пунктом " **инструменты** " исчезает.</span><span class="sxs-lookup"><span data-stu-id="5d958-278">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="5d958-279">Нажмите кнопку **Показать** и выберите **в новом окне** еще раз.</span><span class="sxs-lookup"><span data-stu-id="5d958-279">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    > ##### Old Figure 22  
    > The animation that indicates that the site is getting built  
    > ![The animation that indicates that the site is getting built][ImageBuilding]  
    -->  
    
<span data-ttu-id="5d958-280">Используйте рабочие процессы, которые вы узнали ранее, чтобы вручную проверить, работает ли сжатие.</span><span class="sxs-lookup"><span data-stu-id="5d958-280">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="5d958-281">Вернитесь на вкладку Demo и повторно загрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="5d958-281">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="5d958-282">Столбец « **Размер** » теперь должен показывать 2 разных значения для текстовых ресурсов `bundle.js` , таких как.</span><span class="sxs-lookup"><span data-stu-id="5d958-282">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="5d958-283">На [рисунке 23](#figure-23) верхнее значение аргумента `256 KB` `bundle.js` "равно" — Размер файла, отправленного по сети, а в качестве нижнего значения `1.2 MB` — несжатый размер файла.</span><span class="sxs-lookup"><span data-stu-id="5d958-283">In [Figure 23](#figure-23) the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    > ##### <span data-ttu-id="5d958-284">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="5d958-284">Figure 22</span></span>  
    > <span data-ttu-id="5d958-285">В столбце "размер" теперь показано 2 разных значения для текстовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d958-285">The Size column now shows 2 different values for text resources</span></span>  
    > <span data-ttu-id="5d958-286">! [В столбце "размер" показано 2 разных значения для текстовых ресурсов] [ImageRequests]</span><span class="sxs-lookup"><span data-stu-id="5d958-286">![The Size column now shows 2 different values for text resources][ImageRequests]</span></span>  
    
1.  <span data-ttu-id="5d958-287">В разделе **заголовки ответа** `bundle.js` теперь должен быть указан `content-encoding: gzip` верхний колонтитул.</span><span class="sxs-lookup"><span data-stu-id="5d958-287">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    > ##### <span data-ttu-id="5d958-288">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="5d958-288">Figure 23</span></span>  
    > <span data-ttu-id="5d958-289">Раздел заголовки ответа теперь содержат заголовок Content-Encoding</span><span class="sxs-lookup"><span data-stu-id="5d958-289">The Response Headers section now contains a content-encoding header</span></span>  
    > <span data-ttu-id="5d958-290">! [Раздел заголовков ответа теперь состоит из заголовка Content-Encoding] [ImageGzip]</span><span class="sxs-lookup"><span data-stu-id="5d958-290">![The Response Headers section now contains a content-encoding header][ImageGzip]</span></span>  
    
<span data-ttu-id="5d958-291">Проведите аудит страницы, чтобы оценить, какое влияние сжатие текста влияет на производительность загрузки страницы:</span><span class="sxs-lookup"><span data-stu-id="5d958-291">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="5d958-292">Перейдите на вкладку **Аудит** .</span><span class="sxs-lookup"><span data-stu-id="5d958-292">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="5d958-293">Выберите **аудит выполнения аудита** ![ ][ImagePerformIcon] .</span><span class="sxs-lookup"><span data-stu-id="5d958-293">Select **Perform an audit** ![Perform an audit][ImagePerformIcon].</span></span>  
1.  <span data-ttu-id="5d958-294">Параметры не совпадают.</span><span class="sxs-lookup"><span data-stu-id="5d958-294">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="5d958-295">Нажмите кнопку **запустить аудит**.</span><span class="sxs-lookup"><span data-stu-id="5d958-295">Select **Run audit**.</span></span>  
    
    > ##### <span data-ttu-id="5d958-296">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="5d958-296">Figure 24</span></span>  
    > <span data-ttu-id="5d958-297">Отчет "Аудит" после включения сжатия текста</span><span class="sxs-lookup"><span data-stu-id="5d958-297">An Audits report after enabling text compression</span></span>  
    > <span data-ttu-id="5d958-298">! [Отчет аудита после включения функции сжатия текста] [ImageReport2]</span><span class="sxs-lookup"><span data-stu-id="5d958-298">![An Audits report after enabling text compression][ImageReport2]</span></span>  
    
<span data-ttu-id="5d958-299">Woohoo!</span><span class="sxs-lookup"><span data-stu-id="5d958-299">Woohoo!</span></span>  <span data-ttu-id="5d958-300">Похоже на ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="5d958-300">That looks like progress.</span></span>  <span data-ttu-id="5d958-301">Общая оценка производительности должна быть увеличена, а это значит, что сайт быстрее.</span><span class="sxs-lookup"><span data-stu-id="5d958-301">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="5d958-302">Сжатие текста в реальном мире</span><span class="sxs-lookup"><span data-stu-id="5d958-302">Text compression in the real world</span></span>   

<span data-ttu-id="5d958-303">На большинстве серверов есть простые решения, подобные этим, чтобы включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="5d958-303">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="5d958-304">Просто выполните поиск, чтобы настроить любой сервер, который вы используете для сжатия текста.</span><span class="sxs-lookup"><span data-stu-id="5d958-304">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="5d958-305">Изменение размера изображения</span><span class="sxs-lookup"><span data-stu-id="5d958-305">Resize images</span></span>   

<span data-ttu-id="5d958-306">Отчет о том, что не следует избегать огромных полезных данных сети, является одной из самых первых возможностей для повышения производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-306">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="5d958-307">Изменение размеров изображений помогает уменьшить размер полезных данных в сети.</span><span class="sxs-lookup"><span data-stu-id="5d958-307">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="5d958-308">Если пользователь просматривает изображения на экране мобильного устройства размером 500 в пикселах, это не значит, что при отправке изображения в масштабе не более 1500 точек.</span><span class="sxs-lookup"><span data-stu-id="5d958-308">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="5d958-309">В идеале вы отправляете изображение в 500 в масштабе по пикселю.</span><span class="sxs-lookup"><span data-stu-id="5d958-309">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="5d958-310">В отчете выберите команду **Избегайте огромных полезных данных сети** , чтобы узнать, какие изображения нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5d958-310">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="5d958-311">Похоже, что 2 файлов JPG — более 2000 КБ, что больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="5d958-311">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    > ##### Old Figure 27  
    > Details about the **Properly size images** opportunity  
    > ![Details about the properly size images opportunity][ImageResize]  
    -->

1.  <span data-ttu-id="5d958-312">Вернувшись на вкладку Редактор, открыть `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="5d958-312">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="5d958-313">Заменить `const dir = 'big'` на `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="5d958-313">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="5d958-314">Этот каталог содержит копии тех же изображений, размер которых был изменен.</span><span class="sxs-lookup"><span data-stu-id="5d958-314">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="5d958-315">Вновь проведите аудит страницы, чтобы увидеть, как это изменение влияет на производительность загрузки.</span><span class="sxs-lookup"><span data-stu-id="5d958-315">Audit the page again to see how this change affects load performance.</span></span>  
    
    > ##### <span data-ttu-id="5d958-316">Рис. 25</span><span class="sxs-lookup"><span data-stu-id="5d958-316">Figure 25</span></span>  
    > <span data-ttu-id="5d958-317">Отчет об аудите после изменения размеров изображений</span><span class="sxs-lookup"><span data-stu-id="5d958-317">An Audits report after resizing images</span></span>  
    > <span data-ttu-id="5d958-318">! [Отчет об аудите после изменения размера изображений] [ImageReport3]</span><span class="sxs-lookup"><span data-stu-id="5d958-318">![An Audits report after resizing images][ImageReport3]</span></span>  

<span data-ttu-id="5d958-319">Похоже, что изменение имеет незначительный уровень влияния на общую оценку производительности.</span><span class="sxs-lookup"><span data-stu-id="5d958-319">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="5d958-320">Тем не менее, в этом случае баллы не показываются четко, так как данные сети, которые вы сохраняете, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="5d958-320">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="5d958-321">Общий размер старой фотографии — около 5,3 мегабайт, в то время как теперь это не более 0,18 МБ.</span><span class="sxs-lookup"><span data-stu-id="5d958-321">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="5d958-322">Изменение размеров изображений в реальном мире</span><span class="sxs-lookup"><span data-stu-id="5d958-322">Resizing images in the real world</span></span>   

<span data-ttu-id="5d958-323">В случае с небольшим приложением вы можете использовать один из этих способов, так как это может быть достаточно хорошим.</span><span class="sxs-lookup"><span data-stu-id="5d958-323">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="5d958-324">Но для больших приложений это очевидно не масштабируется.</span><span class="sxs-lookup"><span data-stu-id="5d958-324">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="5d958-325">Ниже приведены некоторые стратегии управления изображениями в крупных приложениях.</span><span class="sxs-lookup"><span data-stu-id="5d958-325">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="5d958-326">Изменение размера изображения во время процесса сборки.</span><span class="sxs-lookup"><span data-stu-id="5d958-326">Resize images during your build process.</span></span>  
*   <span data-ttu-id="5d958-327">Создавайте несколько размеров изображения во время процесса сборки, а затем используйте `srcset` их в коде.</span><span class="sxs-lookup"><span data-stu-id="5d958-327">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="5d958-328">Во время выполнения браузер берет на себя выбор оптимального размера для устройства.</span><span class="sxs-lookup"><span data-stu-id="5d958-328">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->

<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="5d958-329">Использование сети CDN изображений, позволяющей динамически изменять размер изображения при запросе.</span><span class="sxs-lookup"><span data-stu-id="5d958-329">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="5d958-330">По крайней мере, оптимизируйте каждое изображение.</span><span class="sxs-lookup"><span data-stu-id="5d958-330">At the very least, optimize each image.</span></span>  <span data-ttu-id="5d958-331">Это может создать огромный выигрыш.</span><span class="sxs-lookup"><span data-stu-id="5d958-331">This may create huge savings.</span></span>  
  <span data-ttu-id="5d958-332">Оптимизация — это время, когда вы запускаете изображение с помощью специальной программы, которая уменьшает размер файла изображения.</span><span class="sxs-lookup"><span data-stu-id="5d958-332">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="5d958-333">Дополнительные советы приведены в статье основные сведения об [оптимизации изображений][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="5d958-333">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  

### <span data-ttu-id="5d958-334">Исключение ресурсов блокировки рендеринга</span><span class="sxs-lookup"><span data-stu-id="5d958-334">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="5d958-335">В последней версии отчета говорится о том, что в настоящее время ресурсы, блокирующие рендеринг, стали самой большой возможностью.</span><span class="sxs-lookup"><span data-stu-id="5d958-335">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="5d958-336">Ресурс блокировки обработки — это внешний файл JavaScript или CSS, который браузер должен загрузить, проанализировать и выполнить, прежде чем отобразить страницу.</span><span class="sxs-lookup"><span data-stu-id="5d958-336">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="5d958-337">Цель состоит в том, чтобы запустить только основной код CSS и JavaScript, необходимый для правильного отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-337">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="5d958-338">Первая задача — это поиск кода, который не нужно выполнять при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-338">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="5d958-339">Чтобы просмотреть блокируемые ресурсы, выберите пункт **удалить ресурсы блокировки рендеринга** .</span><span class="sxs-lookup"><span data-stu-id="5d958-339">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="5d958-340">и `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="5d958-340">and `jquery.js`.</span></span>  
    
    > ##### <span data-ttu-id="5d958-341">Рис. 26</span><span class="sxs-lookup"><span data-stu-id="5d958-341">Figure 26</span></span>  
    > <span data-ttu-id="5d958-342">Дополнительные сведения о **ресурсах блокировки обработки** с возможностью устранения</span><span class="sxs-lookup"><span data-stu-id="5d958-342">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    > <span data-ttu-id="5d958-343">! [Дополнительные сведения о ресурсах устранения незавершенной обработки с возможностью возможной сделки] [ImageRender]</span><span class="sxs-lookup"><span data-stu-id="5d958-343">![More information about the Eliminate render-blocking resources opportunity][ImageRender]</span></span>  
    
1.  <span data-ttu-id="5d958-344">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, начните вводить текст `Coverage` и выберите пункт **Показать покрытие**.</span><span class="sxs-lookup"><span data-stu-id="5d958-344">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    > ##### <span data-ttu-id="5d958-345">На рисунке 27</span><span class="sxs-lookup"><span data-stu-id="5d958-345">Figure 27</span></span>  
    > <span data-ttu-id="5d958-346">Открытие меню команды на панели «аудит»</span><span class="sxs-lookup"><span data-stu-id="5d958-346">Opening the Command Menu from the Audits panel</span></span>  
    > <span data-ttu-id="5d958-347">! [Открытие меню команд из панели аудита] [ImageCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="5d958-347">![Opening the Command Menu from the Audits panel][ImageCommandMenu]</span></span>  
    
    > ##### <span data-ttu-id="5d958-348">Рис. 28</span><span class="sxs-lookup"><span data-stu-id="5d958-348">Figure 28</span></span>  
    > <span data-ttu-id="5d958-349">Вкладка "покрытие"</span><span class="sxs-lookup"><span data-stu-id="5d958-349">The Coverage tab</span></span>  
    > <span data-ttu-id="5d958-350">! [Вкладка "покрытие"] [ImageCoverage]</span><span class="sxs-lookup"><span data-stu-id="5d958-350">![The Coverage tab][ImageCoverage]</span></span>  
    
1.  <span data-ttu-id="5d958-351">Нажмите кнопку **Обновить** ![ Обновление ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="5d958-351">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="5d958-352">На вкладке " **покрытие** " представлены общие сведения о том, какая часть `bundle.js` кода `jquery.js` и `lodash.js` выполняется при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-352">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="5d958-353">[На рисунке 30](#figure-30) говорится, что около 76% и 30% файлов jQuery и Lodash не используются соответственно.</span><span class="sxs-lookup"><span data-stu-id="5d958-353">[Figure 30](#figure-30) says that about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    > ##### <span data-ttu-id="5d958-354">Рис. 29</span><span class="sxs-lookup"><span data-stu-id="5d958-354">Figure 29</span></span>  
    > <span data-ttu-id="5d958-355">Отчет о покрытии</span><span class="sxs-lookup"><span data-stu-id="5d958-355">The Coverage report</span></span>  
    > <span data-ttu-id="5d958-356">! [Отчет о покрытии] [ImageCoverageReport]</span><span class="sxs-lookup"><span data-stu-id="5d958-356">![The Coverage report][ImageCoverageReport]</span></span>  
    
1.  <span data-ttu-id="5d958-357">Выберите строку **jQuery. js** .</span><span class="sxs-lookup"><span data-stu-id="5d958-357">Select the **jquery.js** row.</span></span>  <span data-ttu-id="5d958-358">DevTools откроет файл на панели «источники».</span><span class="sxs-lookup"><span data-stu-id="5d958-358">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="5d958-359">Строка кода была выполнена, если рядом с ней есть синяя полоска.</span><span class="sxs-lookup"><span data-stu-id="5d958-359">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="5d958-360">Красная черта означает, что она не была выполнена и определенно не требуется при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-360">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    > ##### <span data-ttu-id="5d958-361">Рис. 30</span><span class="sxs-lookup"><span data-stu-id="5d958-361">Figure 30</span></span>  
    > <span data-ttu-id="5d958-362">Просмотр файла jQuery на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="5d958-362">Viewing the jQuery file in the Sources panel</span></span>  
    > <span data-ttu-id="5d958-363">! [Просмотр файла jQuery на панели «источники»] [ImageJQuery]</span><span class="sxs-lookup"><span data-stu-id="5d958-363">![Viewing the jQuery file in the Sources panel][ImageJQuery]</span></span>  
    
1.  <span data-ttu-id="5d958-364">Прокрутите код jQuery на немного.</span><span class="sxs-lookup"><span data-stu-id="5d958-364">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="5d958-365">Некоторые строки, которые получают слово "выполнить", на самом деле представляют собой комментарии.</span><span class="sxs-lookup"><span data-stu-id="5d958-365">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="5d958-366">Выполнение этого кода с помощью Minifier, который содержит примечания, — еще один способ уменьшить размер файла.</span><span class="sxs-lookup"><span data-stu-id="5d958-366">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="5d958-367">Коротко говоря, при работе с собственным кодом вкладка "покрытие" помогает проанализировать код, построчно и поставлять только код, необходимый для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-367">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="5d958-368">Нужны ли `jquery.js` `lodash.js` файлы и даже для загрузки страницы?</span><span class="sxs-lookup"><span data-stu-id="5d958-368">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="5d958-369">На вкладке Блокировка запроса показано, что происходит, когда ресурсы недоступны.</span><span class="sxs-lookup"><span data-stu-id="5d958-369">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="5d958-370">Откройте вкладку **сеть** .</span><span class="sxs-lookup"><span data-stu-id="5d958-370">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="5d958-371">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы снова открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="5d958-371">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="5d958-372">Начните вводить данные `blocking` и установите флажок **Показать блокировку запросов**.</span><span class="sxs-lookup"><span data-stu-id="5d958-372">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    > ##### <span data-ttu-id="5d958-373">На рисунке 31</span><span class="sxs-lookup"><span data-stu-id="5d958-373">Figure 31</span></span>  
    > <span data-ttu-id="5d958-374">Вкладка "блокировка запросов"</span><span class="sxs-lookup"><span data-stu-id="5d958-374">The Request Blocking tab</span></span>  
    > <span data-ttu-id="5d958-375">! [Вкладка блокировки запросов] [ImageBlocking]</span><span class="sxs-lookup"><span data-stu-id="5d958-375">![The Request Blocking tab][ImageBlocking]</span></span>  
    
1.  <span data-ttu-id="5d958-376">Нажмите кнопку **Добавить узор** ![ ][ImageAddPatternIcon] , введите текст `/libs/*` , а затем нажмите кнопку `Enter` для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5d958-376">Select **Add Pattern** ![Add Pattern][ImageAddPatternIcon], type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    > ##### <span data-ttu-id="5d958-377">Рисунок 32</span><span class="sxs-lookup"><span data-stu-id="5d958-377">Figure 32</span></span>  
    > <span data-ttu-id="5d958-378">Добавление шаблона для блокирования запросов в `libs` Каталог</span><span class="sxs-lookup"><span data-stu-id="5d958-378">Adding a pattern to block any request to the `libs` directory</span></span>  
    > <span data-ttu-id="5d958-379">! [Добавление шаблона для блокирования запросов в каталог библиотек] [ImageLibs]</span><span class="sxs-lookup"><span data-stu-id="5d958-379">![Adding a pattern to block any request to the libs directory][ImageLibs]</span></span>  
    
1.  <span data-ttu-id="5d958-380">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="5d958-380">Refresh the page.</span></span>  <span data-ttu-id="5d958-381">Запросы jQuery и Lodash красного цвета, означающие, что запросы были заблокированы.</span><span class="sxs-lookup"><span data-stu-id="5d958-381">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="5d958-382">Страница по-прежнему загружается и является интерактивной, поэтому она выглядит так, как это не требуется.</span><span class="sxs-lookup"><span data-stu-id="5d958-382">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    > ##### <span data-ttu-id="5d958-383">Рисунок 33</span><span class="sxs-lookup"><span data-stu-id="5d958-383">Figure 33</span></span>  
    > <span data-ttu-id="5d958-384">На панели Network (сеть) показано, что запросы заблокированы</span><span class="sxs-lookup"><span data-stu-id="5d958-384">The Network panel shows that the requests have been blocked</span></span>  
    > <span data-ttu-id="5d958-385">! [На панели Network (сеть) показано, что запросы заблокированы] [ImageBlockedLibs]</span><span class="sxs-lookup"><span data-stu-id="5d958-385">![The Network panel shows that the requests have been blocked][ImageBlockedLibs]</span></span>  
    
1.  <span data-ttu-id="5d958-386">Нажмите кнопку **удалить все шаблоны** ![ . Удалите все шаблоны, ][ImageRemoveIcon] чтобы удалить `/libs/*` шаблон блокировки.</span><span class="sxs-lookup"><span data-stu-id="5d958-386">Select **Remove all patterns** ![Remove all patterns][ImageRemoveIcon] to delete the `/libs/*` blocking pattern.</span></span>  

<span data-ttu-id="5d958-387">Как правило, вкладка "блокировка запросов" полезна для имитации того, как работает страница, если какой-либо из указанных ресурсов недоступен.</span><span class="sxs-lookup"><span data-stu-id="5d958-387">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="5d958-388">Теперь удалите ссылки на эти файлы из кода и выполните аудит страницы еще раз:</span><span class="sxs-lookup"><span data-stu-id="5d958-388">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="5d958-389">Вернувшись на вкладку Редактор, открыть `template.html` .</span><span class="sxs-lookup"><span data-stu-id="5d958-389">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="5d958-390">Удалите `<script src="/libs/lodash.js">` и `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="5d958-390">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="5d958-391">Дождитесь повторного создания и повторного развертывания сайта.</span><span class="sxs-lookup"><span data-stu-id="5d958-391">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="5d958-392">Снова проведите аудит страницы с помощью панели **аудита** .</span><span class="sxs-lookup"><span data-stu-id="5d958-392">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="5d958-393">Ваши общие баллы должны быть улучшены.</span><span class="sxs-lookup"><span data-stu-id="5d958-393">Your overall score should have improved again.</span></span>  
    
    > ##### <span data-ttu-id="5d958-394">Рисунок 34</span><span class="sxs-lookup"><span data-stu-id="5d958-394">Figure 34</span></span>  
    > <span data-ttu-id="5d958-395">Отчет об аудите после удаления ресурсов блокировки рендеринга</span><span class="sxs-lookup"><span data-stu-id="5d958-395">An Audits report after removing the render-blocking resources</span></span>  
    > <span data-ttu-id="5d958-396">! [Отчет аудита после удаления ресурсов блокировки рендеринга] [ImageReport4]</span><span class="sxs-lookup"><span data-stu-id="5d958-396">![An Audits report after removing the render-blocking resources][ImageReport4]</span></span>  

#### <span data-ttu-id="5d958-397">Оптимизация критического пути отрисовки в реальном мире</span><span class="sxs-lookup"><span data-stu-id="5d958-397">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="5d958-398">**Критический путь рендеринга** указывает на код, необходимый для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-398">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="5d958-399">Как правило, скорость загрузки страницы повышается за счет отправки критического кода только при загрузке страницы, а затем — через отложенную загрузку всех остальных.</span><span class="sxs-lookup"><span data-stu-id="5d958-399">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="5d958-400">Маловероятно, что вы можете найти сценарии, которые можно удалить прямо, но вы можете найти большое количество сценариев, которые вам не нужно запрашивать во время загрузки страницы, и, возможно, они будут запрашиваться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="5d958-400">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="5d958-401">Если вы используете платформу, убедитесь в том, что у нее есть производственный режим.</span><span class="sxs-lookup"><span data-stu-id="5d958-401">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="5d958-402">Этот режим может использовать такие функции, как [Tree встряхнув][WebpackTreeShaking] , для удаления ненужного кода, блокирующего критический рендеринг.</span><span class="sxs-lookup"><span data-stu-id="5d958-402">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  

<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="5d958-403">Работа менее основного потока</span><span class="sxs-lookup"><span data-stu-id="5d958-403">Do less main thread work</span></span>   

<span data-ttu-id="5d958-404">В последней версии отчета представлены некоторые небольшие возможности по экономии средств в разделе "возможности", но если вы просмотрии раздел "Диагностика", это похоже на то, что наибольший узкий участок слишком велик для основного потока.</span><span class="sxs-lookup"><span data-stu-id="5d958-404">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="5d958-405">Основной поток — это тот случай, когда браузер выполняет большую часть работы, необходимой для отображения страницы, например синтаксического анализа и выполнения HTML, CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d958-405">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="5d958-406">Цель состоит в том, чтобы проанализировать трудозатраты, выполняемые основным потоком при загрузке страницы, и найти способы задержать или удалить ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="5d958-406">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="5d958-407">Откройте вкладку **производительность** .</span><span class="sxs-lookup"><span data-stu-id="5d958-407">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="5d958-408">Выберите параметры захвата **параметров** ![ ][ImageCaptureIcon] .</span><span class="sxs-lookup"><span data-stu-id="5d958-408">Select **Capture Settings** ![Capture Settings][ImageCaptureIcon].</span></span>  
1.  <span data-ttu-id="5d958-409">Настройте **сеть** на **медленное 3G** и **ЦП** , чтобы **6X замедление**.</span><span class="sxs-lookup"><span data-stu-id="5d958-409">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="5d958-410">На мобильных устройствах обычно используются больше ограничений на оборудование, чем на ноутбуках или настольных компьютерах, поэтому эти параметры позволяют загрузить страницу так, как если бы вы использовали менее мощное устройство.</span><span class="sxs-lookup"><span data-stu-id="5d958-410">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="5d958-411">Нажмите кнопку **Обновить** ![ Обновление ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="5d958-411">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="5d958-412">DevTools обновляет страницу и создает визуализацию всей выполненной работы, чтобы загрузить страницу.</span><span class="sxs-lookup"><span data-stu-id="5d958-412">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="5d958-413">Этот зрительный образ называется **трассировкой**.</span><span class="sxs-lookup"><span data-stu-id="5d958-413">This visualization is referred to as the **trace**.</span></span>  
    
    > ##### <span data-ttu-id="5d958-414">Рисунок 35</span><span class="sxs-lookup"><span data-stu-id="5d958-414">Figure 35</span></span>  
    > <span data-ttu-id="5d958-415">Трассировка загрузки страницы на панели производительности</span><span class="sxs-lookup"><span data-stu-id="5d958-415">The Performance panel trace of the page load</span></span>  
    > <span data-ttu-id="5d958-416">! [Трассировка панели «производительность» для загрузки страницы] [ImagePerformance]</span><span class="sxs-lookup"><span data-stu-id="5d958-416">![The Performance panel trace of the page load][ImagePerformance]</span></span>  

<span data-ttu-id="5d958-417">Трассировка отображает операцию в хронологическом порядке, слева направо.</span><span class="sxs-lookup"><span data-stu-id="5d958-417">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="5d958-418">На диаграммах с частотой кадров, ЦП и нетто в верхней части экрана дается обзор кадров в секунду, активности ЦП и активности сети.</span><span class="sxs-lookup"><span data-stu-id="5d958-418">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="5d958-419">Выделенный блок желтого цвета, показанный на [рисунке 37](#figure-37) , означает, что ЦП полностью загружен с действиями в сценариях.</span><span class="sxs-lookup"><span data-stu-id="5d958-419">The block of yellow selected that you see in [Figure 37](#figure-37) means that the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="5d958-420">Это говорит о том, что вы можете ускорить загрузку страницы, выполнив меньше действий JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d958-420">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

> ##### <span data-ttu-id="5d958-421">Рисунок 36</span><span class="sxs-lookup"><span data-stu-id="5d958-421">Figure 36</span></span>  
> <span data-ttu-id="5d958-422">Раздел обзора трассировки</span><span class="sxs-lookup"><span data-stu-id="5d958-422">The Overview section of the trace</span></span>  
> <span data-ttu-id="5d958-423">! [Раздел обзора трассировки] [ImageOverview]</span><span class="sxs-lookup"><span data-stu-id="5d958-423">![The Overview section of the trace][ImageOverview]</span></span>  

<span data-ttu-id="5d958-424">Изучите трассировку, чтобы найти способы выполнения меньшей работы в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d958-424">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="5d958-425">Щелкните раздел **время показа** , чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="5d958-425">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="5d958-426">В зависимости от того факта, что существует ряд мер [времени][MDNUserTimingApi] , не отклика, может показаться, что приложение Илья использует режим разработки реагируй.</span><span class="sxs-lookup"><span data-stu-id="5d958-426">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="5d958-427">Переключение в режим рабочего режима может привести к снижению производительности WINS.</span><span class="sxs-lookup"><span data-stu-id="5d958-427">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    > ##### <span data-ttu-id="5d958-428">Рисунок 37</span><span class="sxs-lookup"><span data-stu-id="5d958-428">Figure 37</span></span>  
    > <span data-ttu-id="5d958-429">Раздел "временные интервалы"</span><span class="sxs-lookup"><span data-stu-id="5d958-429">The Timings section</span></span>  
    > <span data-ttu-id="5d958-430">! [Раздел временных интервалов] [ImageUserTiming]</span><span class="sxs-lookup"><span data-stu-id="5d958-430">![The Timings section][ImageUserTiming]</span></span>  

1.  <span data-ttu-id="5d958-431">Чтобы свернуть этот раздел, выберите пункт **время показа** .</span><span class="sxs-lookup"><span data-stu-id="5d958-431">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="5d958-432">Просмотрите **основной** раздел.</span><span class="sxs-lookup"><span data-stu-id="5d958-432">Browse the **Main** section.</span></span>  <span data-ttu-id="5d958-433">В этом разделе показан хронологический журнал основных операций потока, слева направо.</span><span class="sxs-lookup"><span data-stu-id="5d958-433">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="5d958-434">Ось y (сверху вниз) показывает причины возникновения событий.</span><span class="sxs-lookup"><span data-stu-id="5d958-434">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="5d958-435">Например, на [рисунке 39](#figure-39) `Evaluate Script` событие привело к `(anonymous)` выполнению функции, которая вызывает запуск `(anonymous)` `__webpack__require__` и т. д.</span><span class="sxs-lookup"><span data-stu-id="5d958-435">For example, in [Figure 39](#figure-39), the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    > ##### <span data-ttu-id="5d958-436">Рисунок 38</span><span class="sxs-lookup"><span data-stu-id="5d958-436">Figure 38</span></span>  
    > <span data-ttu-id="5d958-437">Основной раздел</span><span class="sxs-lookup"><span data-stu-id="5d958-437">The Main section</span></span>  
    > <span data-ttu-id="5d958-438">! [Основной раздел] [ImageMain]</span><span class="sxs-lookup"><span data-stu-id="5d958-438">![The Main section][ImageMain]</span></span>  

1.  <span data-ttu-id="5d958-439">Прокрутите страницу вниз до конца **основного** раздела.</span><span class="sxs-lookup"><span data-stu-id="5d958-439">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="5d958-440">При использовании платформы большая часть верхнего действия вызывается платформой, которая обычно находится в вашем элементе управления.</span><span class="sxs-lookup"><span data-stu-id="5d958-440">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="5d958-441">Действия, вызванные вашим приложением, обычно находятся в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="5d958-441">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="5d958-442">В этом приложении это похоже на функцию с именем, которая `App` вызывает большое количество запросов к `mineBitcoin` функции.</span><span class="sxs-lookup"><span data-stu-id="5d958-442">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="5d958-443">Это звучит так, как Илья может использовать устройства своего вентилятора для cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="5d958-443">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    > ##### <span data-ttu-id="5d958-444">Рисунок 39</span><span class="sxs-lookup"><span data-stu-id="5d958-444">Figure 39</span></span>  
    > <span data-ttu-id="5d958-445">Наведение указателя мыши на `mineBitcoin` действие</span><span class="sxs-lookup"><span data-stu-id="5d958-445">Hovering over the `mineBitcoin` activity</span></span>  
    > <span data-ttu-id="5d958-446">! [Наведите указатель мыши на действие mineBitcoin] [ImageMine]</span><span class="sxs-lookup"><span data-stu-id="5d958-446">![Hovering over the mineBitcoin activity][ImageMine]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5d958-447">Несмотря на то что запросы вашей платформы обычно прерываются из вашего элемента управления, иногда вы можете структурировать приложение таким образом, чтобы она выполнялась неэффективно.</span><span class="sxs-lookup"><span data-stu-id="5d958-447">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="5d958-448">Реструктуризация приложения для эффективного использования инфраструктуры — это способ выполнения менее основного потока работ.</span><span class="sxs-lookup"><span data-stu-id="5d958-448">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="5d958-449">Тем не менее, для этого необходимо глубокое понимание того, как работает ваша платформа, и какие изменения вносятся в вашем собственном коде для более эффективной работы с платформой.</span><span class="sxs-lookup"><span data-stu-id="5d958-449">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  

1.  <span data-ttu-id="5d958-450">Разверните раздел **снизу вверх** .</span><span class="sxs-lookup"><span data-stu-id="5d958-450">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="5d958-451">На этой вкладке прерываются действия, которые выполнялись в течение всего времени.</span><span class="sxs-lookup"><span data-stu-id="5d958-451">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="5d958-452">Если в разделе снизу вверх ничего не видно, щелкните надпись для **основного** раздела.</span><span class="sxs-lookup"><span data-stu-id="5d958-452">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="5d958-453">В разделе " **снизу вверх** " отображаются только сведения о каких-либо действиях или группах действий, которые вы уже выбрали.</span><span class="sxs-lookup"><span data-stu-id="5d958-453">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="5d958-454">Например, если вы `mineBitcoin` **настроили** одно из действий, в разделе снизу вверх будет отображаться только информация для этого действия.</span><span class="sxs-lookup"><span data-stu-id="5d958-454">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    > ##### <span data-ttu-id="5d958-455">Рисунок 40</span><span class="sxs-lookup"><span data-stu-id="5d958-455">Figure 40</span></span>  
    > <span data-ttu-id="5d958-456">Вкладка "снизу вверх"</span><span class="sxs-lookup"><span data-stu-id="5d958-456">The Bottom-Up tab</span></span>  
    > <span data-ttu-id="5d958-457">! [Вкладка "снизу вверх"] [ImageBottomUp]</span><span class="sxs-lookup"><span data-stu-id="5d958-457">![The Bottom-Up tab][ImageBottomUp]</span></span>  

<span data-ttu-id="5d958-458">В столбце " **собственное время** " показано, сколько времени было затрачено непосредственно на каждое действие.</span><span class="sxs-lookup"><span data-stu-id="5d958-458">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="5d958-459">Например, на [рисунке 41](#figure-41) показано, что в функции было затрачено около 63% времени основного потока `mineBitcoin` .</span><span class="sxs-lookup"><span data-stu-id="5d958-459">For example, [Figure 41](#figure-41) shows that about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="5d958-460">Время от времени до того, чтобы узнать, используется ли производственный режим и уменьшается активность JavaScript, может ускорить загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-460">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="5d958-461">Начните работу в режиме "в производство":</span><span class="sxs-lookup"><span data-stu-id="5d958-461">Start with production mode:</span></span>  

1.  <span data-ttu-id="5d958-462">На вкладке Редактор откройте `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="5d958-462">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="5d958-463">Заменить `"mode":"development"` на `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="5d958-463">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="5d958-464">Дождитесь завершения развертывания новой сборки.</span><span class="sxs-lookup"><span data-stu-id="5d958-464">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="5d958-465">Вновь проведите аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-465">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="5d958-466">Рисунок 41</span><span class="sxs-lookup"><span data-stu-id="5d958-466">Figure 41</span></span>  
    > <span data-ttu-id="5d958-467">Отчет по аудиту после настройки пакета для использования режима "в производство"</span><span class="sxs-lookup"><span data-stu-id="5d958-467">An Audits report after configuring webpack to use production mode</span></span>  
    > <span data-ttu-id="5d958-468">! [Отчет по аудиту после настройки пакета для использования в режиме "производство"] [ImageReport5]</span><span class="sxs-lookup"><span data-stu-id="5d958-468">![An Audits report after configuring webpack to use production mode][ImageReport5]</span></span>  

<span data-ttu-id="5d958-469">Сокращение действий JavaScript путем удаления запроса на `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="5d958-469">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="5d958-470">На вкладке Редактор откройте `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="5d958-470">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="5d958-471">Закомментируйте запрос `this.mineBitcoin(1500)` в `constructor` .</span><span class="sxs-lookup"><span data-stu-id="5d958-471">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="5d958-472">Дождитесь завершения развертывания новой сборки.</span><span class="sxs-lookup"><span data-stu-id="5d958-472">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="5d958-473">Вновь проведите аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="5d958-473">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="5d958-474">Рисунок 42</span><span class="sxs-lookup"><span data-stu-id="5d958-474">Figure 42</span></span>  
    > <span data-ttu-id="5d958-475">Отчет по аудиту после удаления ненужных действий JavaScript</span><span class="sxs-lookup"><span data-stu-id="5d958-475">An Audits report after removing unnecessary JavaScript work</span></span>  
    > <span data-ttu-id="5d958-476">! [Отчет аудита после удаления ненужных действий JavaScript] [ImageReport6]</span><span class="sxs-lookup"><span data-stu-id="5d958-476">![An Audits report after removing unnecessary JavaScript work][ImageReport6]</span></span>  

<span data-ttu-id="5d958-477">Похоже, что Последнее изменение вызвало значительный переход в производительности!</span><span class="sxs-lookup"><span data-stu-id="5d958-477">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="5d958-478">Этот раздел предоставил краткое введение в панель производительности.</span><span class="sxs-lookup"><span data-stu-id="5d958-478">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="5d958-479">Дополнительные сведения о том, как анализировать производительность страниц, можно найти в статье [Анализ производительности][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="5d958-479">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="5d958-480">Выполнение менее основного потока работ в реальном мире</span><span class="sxs-lookup"><span data-stu-id="5d958-480">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="5d958-481">Как правило, панель **производительности** является наиболее распространенным способом для понимания того, какие действия выполняет загружаемый сайт, и Узнайте о способах удаления ненужных действий.</span><span class="sxs-lookup"><span data-stu-id="5d958-481">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="5d958-482">Если вы предпочитаете использовать более похожий подход `console.log()` , Пользовательский API для работы с [временными][MDNUserTimingApi] сведениями позволяет вам произвольно помечать определенные этапы жизненного цикла приложения, чтобы отслеживать продолжительность каждого из этих фаз.</span><span class="sxs-lookup"><span data-stu-id="5d958-482">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="5d958-483">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5d958-483">Summary</span></span>   

*   <span data-ttu-id="5d958-484">Каждый раз, когда вы задаете оптимальное качество нагрузки для сайта, всегда начинайте с аудита.</span><span class="sxs-lookup"><span data-stu-id="5d958-484">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="5d958-485">Аудит определяет базовые показатели и предоставляет советы по улучшению.</span><span class="sxs-lookup"><span data-stu-id="5d958-485">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="5d958-486">За один раз сделайте одно изменение и проведите аудит страницы после каждого изменения, чтобы увидеть, как это изолированное изменение влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="5d958-486">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--    -->  



<!-- image links -->  

[ImageAddPatternIcon]: /microsoft-edge/devtools-guide-chromium/media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-panels-icon.msft.png  
[ImagePerformIcon]: /microsoft-edge/devtools-guide-chromium/media/perform-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRemoveIcon]: /microsoft-edge/devtools-guide-chromium/media/remove-icon.msft.png  

[ImageTony]: /microsoft-edge/devtools-guide-chromium/media/speed-tony.msft.png "Рисунок 1: Илья CAT"  
[ImageEditor]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js.msft.png "Рисунок 2: вкладка "редактор""  
[ImageMenu]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js-remix-project.msft.png "Рисунок 3: меню, которое появляется после нажатия кнопки Илья"  
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live.msft.png "Рисунок 4: вкладка "демонстрация""  
[ImageDevtools]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live-console.msft.png "Рисунок 5: DevTools и демонстрация"  
[ImageUndocked]: /microsoft-edge/devtools-guide-chromium/media/speed-console.msft.png "Рисунок 6: незакрепленный DevTools"  
[ImageAudits]: /microsoft-edge/devtools-guide-chromium/media/speed-audits-performance.msft.png "Рисунок 7: панель «аудит»"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png "Рисунок 8: отчет для панели «аудит» для производительности сайта"  
<!--[ImageError]: /microsoft-edge/devtools-guide-chromium/media/speed-.msft.png "Old Figure 9: A report that errored"  -->  
[ImageOverall]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-Metrics-Collapsed-Metrics-highlighted.MSFT.png "Рисунок 9: общий показатель эффективности"  
[ImageMetrics]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-Metrics-Collapsed-highlighted.MSFT.png "Рисунок 10: Раздел метрик"  
[ImageFirstMeaningfulPaint]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-Metrics-Expanded.MSFT.png "Рисунок 11: щелкните выделенный выключатель, чтобы развернуть элементы метрик".  
[ImageScreenshots]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-View-Trace.MSFT.png "Рисунок 12: снимки экрана, посвященные загрузке страницы  
[ImageOpportunities]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-Opportunities.MSFT.png "Рисунок 13: раздел" возможности "  
[ImageCompression]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-Opportunities-Expanded.MSFT.png "Рисунок 14: отключение ресурсов блокировки обработки" Возможная сделка "  
[ImageReference]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Web-Dev-Performance-audits.MSFT.png "Рисунок 15: Документация по устранению блокировок ресурсов с блокировкой рендеринга"  
[ImageDiagnostics]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-Diagnostics.MSFT.png "Рисунок 16: раздел" Диагностика "  
[ImagePassed]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-audits-Performance-Passed-audits.MSFT.png "Рисунок 17: раздел" пройденные аудиты "  
[ImageNetwork]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Network.MSFT.png "Рисунок 18: панель" сеть ""  
[ImageLargeRows]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Network-use-Large-Request-Rows.MSFT.png "Рисунок 19: большие строки в таблице" сетевые запросы "  
[ImageHeaders]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Network-use-Large-Request-Rows-Bundle-JS.MSFT.png "Рисунок 20: вкладка" заголовки "  
[ImageServer]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Server-JS.MSFT.png "Рисунок 21: Редактирование Server. js"  
<!--[ImageBuilding]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-server-js-edited.msft.png "Old Figure 22: The animation that indicates that the site is getting built"  -->  
[ImageRequests]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Network-Main.MSFT.png "рис 22: в столбце" размер "теперь показано 2 разных значения для текстовых ресурсов.  
[ImageGzip]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Network-Bundle-JS-Headers-Response.MSFT.png "Рисунок 23: раздел заголовков ответа теперь включает `content-encoding` верхний колонтитул"  
[ImageReport2]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-audits-Performance.MSFT.png "Рисунок 24: отчет аудита после включения сжатия текста"  
<!--[ImageResize]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png "Old Figure 27: Details about the properly size images opportunity"  -->
[ImageReport3]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Compression-Small-Images-audits-Performance.MSFT.png "Рисунок 25: отчет аудита после изменения размера изображений"  
[ImageRender]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-audits-Performance-oppportunities-Expanded.MSFT.png "Рисунок 26: Дополнительные сведения о ресурсах, блокирующем рендеринге, возможностях"  
[ImageCommandMenu]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-audits-Performance-oppportunities-Expanded-Command-Coverage.MSFT.png "Рисунок 27: Открытие меню команд на панели" audits ""  
[ImageCoverage]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-audits-Performance-oppportunities-Expanded-drawer-Coverage.MSFT.png "Рисунок 28: вкладка" покрытие "  
[ImageCoverageReport]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-audits-Performance-oppportunities-Expanded-drawer-Coverage-Reloaded.MSFT.png "Рисунок 29: отчет о покрытии"  
[ImageJQuery]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-Sources-drawer-Coverage-Reloaded-jQuery-JS.MSFT.png "Рисунок 30: Просмотр файла jQuery на панели" источники "  
[ImageBlocking]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-Network-drawer-Request-Blocking-Empty.MSFT.png "Рисунок 31: вкладка" Блокировка запроса "  
[ImageLibs]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-Network-drawer-Request-Blocking-added.MSFT.png "Рисунок 32: Добавление шаблона для блокирования запросов в каталог библиотек"  
[ImageBlockedLibs]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-Network-Reloaded-drawer-Request-Blocking-added.MSFT.png "Рисунок 33: на панели" сеть "показано, что запросы заблокированы"  
[ImageReport4]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-2-audits-Performance.MSFT.png "Рисунок 34: отчет аудита после удаления ресурсов блокировки рендеринга"  
[ImagePerformance]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Performance-Slow-network-Slow-CPU.MSFT.png "Рисунок 35: трассировка панели" производительность "загрузки страницы"  
[ImageOverview]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Performance-Slow-network-Slow-CPU-Main-Highlight.MSFT.png "Рисунок 36: раздел обзора трассировки"  
[ImageUserTiming]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Performance-Slow-network-Slow-CPU-timings.MSFT.png "Рисунок 37: раздел" временные показатели "  
[ImageMain]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Performance-Slow-network-Slow-CPU-Main.MSFT.png "Рисунок 38: основной раздел"  
[ImageMine]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Performance-Slow-network-Slow-CPU-timings-minebitcoin.MSFT.png "Рисунок 39: наведите указатель мыши на действие mineBitcoin"  
[ImageBottomUp]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-Performance-Slow-network-Slow-CPU-timings-Summary-minebitcoin.MSFT.png "Рисунок 40: вкладка" снизу вверх "  
[ImageReport5]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-3-audits-Performance.MSFT.png "Рисунок 41: отчет по аудиту после настройки пакета для использования режима" производство "  
[ImageReport6]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Speed-Glitch-Tony-Remix-updated-4-audits-Performance.MSFT.png "Рисунок 42: отчет аудита после удаления ненужных действий JavaScript"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Справочные материалы по анализу производительности"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Знакомство с классом веб-разработки | Coursera"  

[EssentialImageOptimization]: https://images.guide "Оптимизация изображений"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Директивы-кодировка содержимого | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API времени пользователя | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Tree встряхнув | упаковать"  

> [!NOTE]
> <span data-ttu-id="5d958-535">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d958-535">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5d958-536">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5d958-536">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5d958-538">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d958-538">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

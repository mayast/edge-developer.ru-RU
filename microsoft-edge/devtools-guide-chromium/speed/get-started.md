---
title: Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 42b742316ccaa64aa35fc1d21c5277e448b2d5b7
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984764"
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





# <span data-ttu-id="70b0d-103">Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="70b0d-103">Optimize website speed with Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="70b0d-104">Цель учебника</span><span class="sxs-lookup"><span data-stu-id="70b0d-104">Goal of tutorial</span></span>  

<span data-ttu-id="70b0d-105">В этом учебнике объясняется, как использовать Microsoft Edge DevTools, чтобы найти способы быстрой загрузки веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="70b0d-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="70b0d-106">Что вам понадобится</span><span class="sxs-lookup"><span data-stu-id="70b0d-106">Prerequisites</span></span>  

*   <span data-ttu-id="70b0d-107">У вас должен быть базовый интерфейс разработки веб-приложений, аналогично тому, что научились в этом [Знакомство с классом веб-разработки][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="70b0d-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="70b0d-108">Вам ничего не нужно знать о быстродействии нагрузки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="70b0d-109">В этом учебнике вы узнаете об этом.</span><span class="sxs-lookup"><span data-stu-id="70b0d-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="70b0d-110">Введение</span><span class="sxs-lookup"><span data-stu-id="70b0d-110">Introduction</span></span>   

<span data-ttu-id="70b0d-111">Это Илья.</span><span class="sxs-lookup"><span data-stu-id="70b0d-111">This is Tony.</span></span>  <span data-ttu-id="70b0d-112">Илья чрезвычайно знаменита в отношении Cat общества.</span><span class="sxs-lookup"><span data-stu-id="70b0d-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="70b0d-113">Он создал веб-сайт, чтобы его вентиляторы могли узнать о своем любимом продуктов.</span><span class="sxs-lookup"><span data-stu-id="70b0d-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="70b0d-114">Его вентиляторы понравятся на сайте, но в Илья сохраняются жалобы, которые медленно загружаются на сайт.</span><span class="sxs-lookup"><span data-stu-id="70b0d-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="70b0d-115">Илья предложит вам помочь ему ускорить работу сайта.</span><span class="sxs-lookup"><span data-stu-id="70b0d-115">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Илья CAT" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="70b0d-117">Илья CAT</span><span class="sxs-lookup"><span data-stu-id="70b0d-117">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="70b0d-118">Действие 1: аудит сайта</span><span class="sxs-lookup"><span data-stu-id="70b0d-118">Step 1: Audit the site</span></span>   

<span data-ttu-id="70b0d-119">Всякий раз, когда вы захотите улучшить производительность загрузки сайта, **всегда начинайте с аудита**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-119">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="70b0d-120">Аудитория имеет 2 важные функции.</span><span class="sxs-lookup"><span data-stu-id="70b0d-120">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="70b0d-121">Она создает **базовый план** для измерения последующих изменений.</span><span class="sxs-lookup"><span data-stu-id="70b0d-121">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="70b0d-122">Здесь вы найдете **Советы** , которые помогут вам изменить наиболее благоприятные изменения.</span><span class="sxs-lookup"><span data-stu-id="70b0d-122">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="70b0d-123">Настройка</span><span class="sxs-lookup"><span data-stu-id="70b0d-123">Set up</span></span>   

<span data-ttu-id="70b0d-124">Сначала необходимо настроить сайт, чтобы вы могли вносить в него изменения позже.</span><span class="sxs-lookup"><span data-stu-id="70b0d-124">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="70b0d-125">[Откройте исходный код для сайта](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="70b0d-125">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="70b0d-126">Эта вкладка называется **вкладкой "редактор"**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-126">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Вкладка "редактор"" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="70b0d-128">**Вкладка "редактор"**</span><span class="sxs-lookup"><span data-stu-id="70b0d-128">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-129">Выберите **Илья**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-129">Select **tony**.</span></span>  <span data-ttu-id="70b0d-130">Откроется меню.</span><span class="sxs-lookup"><span data-stu-id="70b0d-130">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Меню, которое появляется после нажатия кнопки Илья" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="70b0d-132">Меню, которое появляется после нажатия кнопки **Илья**</span><span class="sxs-lookup"><span data-stu-id="70b0d-132">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-133">Выберите **Remix проект**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-133">Select **Remix Project**.</span></span>  <span data-ttu-id="70b0d-134">Имя проекта меняется с **Илья** на случайное сгенерированное имя.</span><span class="sxs-lookup"><span data-stu-id="70b0d-134">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="70b0d-135">Теперь у вас есть Редактируемая копия кода.</span><span class="sxs-lookup"><span data-stu-id="70b0d-135">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="70b0d-136">Позже вы можете внести изменения в этот код.</span><span class="sxs-lookup"><span data-stu-id="70b0d-136">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="70b0d-137">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-137">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="70b0d-138">Демонстрационный ролик откроется на новой вкладке.  Эта вкладка упоминается как **вкладка Demo**.  Загрузка сайта может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="70b0d-138">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Вкладка "демонстрация"" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="70b0d-140">Вкладка "демонстрация"</span><span class="sxs-lookup"><span data-stu-id="70b0d-140">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-141">Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="70b0d-141">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="70b0d-142">Рядом с демоном DevTools откроется Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70b0d-142">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools и демонстрация" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="70b0d-144">DevTools и демонстрация</span><span class="sxs-lookup"><span data-stu-id="70b0d-144">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70b0d-145">Для остальных снимков экрана в этом учебнике DevTools отображается в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="70b0d-145">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="70b0d-146">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите его `Undock` и выберите команду **открепить в отдельном окне**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-146">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Незакрепленные DevTools" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="70b0d-148">Незакрепленные DevTools</span><span class="sxs-lookup"><span data-stu-id="70b0d-148">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="70b0d-149">Создание базового плана</span><span class="sxs-lookup"><span data-stu-id="70b0d-149">Establish a baseline</span></span>   

<span data-ttu-id="70b0d-150">Базовый план — это запись того, как выполняется сайт, прежде чем вы внесли улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="70b0d-150">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="70b0d-151">Перейдите на вкладку **Аудит** .  Она может быть скрыта за кнопкой " **Дополнительные панели** " \ "дополнительные панели ![ ][ImageMorePanelsIcon] \".</span><span class="sxs-lookup"><span data-stu-id="70b0d-151">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="70b0d-152">На этой панели есть Lighthouse, так как проект, который включает панель «аудиты», называется **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-152">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Панель «аудит»" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="70b0d-154">Панель « **Аудит** »</span><span class="sxs-lookup"><span data-stu-id="70b0d-154">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="70b0d-155">Соответствие параметров конфигурации аудита с параметрами, приведенными на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="70b0d-155">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="70b0d-156">Ниже приведено описание различных параметров.</span><span class="sxs-lookup"><span data-stu-id="70b0d-156">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="70b0d-157">**Устройства**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-157">**Device**.</span></span>  <span data-ttu-id="70b0d-158">При настройке на **мобильном устройстве** изменяется строка агента пользователя и имитируется мобильное окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="70b0d-158">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="70b0d-159">Настройка для **настольного компьютера** очень просто отключает изменения на **мобильном устройстве** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-159">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="70b0d-160">**Аудита**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-160">**Audits**.</span></span>  <span data-ttu-id="70b0d-161">Отключение категории не позволяет панели аудита выполнять эти проверки и исключает из отчета эти проверки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-161">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="70b0d-162">Если вы хотите просмотреть предоставленные типы рекомендаций, оставьте другие доступные категории.</span><span class="sxs-lookup"><span data-stu-id="70b0d-162">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="70b0d-163">Отключение категорий немного ускоряет процесс аудита.</span><span class="sxs-lookup"><span data-stu-id="70b0d-163">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="70b0d-164">**Регулирование**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-164">**Throttling**.</span></span>  <span data-ttu-id="70b0d-165">Для **эмуляции медленного 4G, скорость процессора 4X** эмулирует типичные условия обзора на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="70b0d-165">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="70b0d-166">Она называется смоделированной, так как панель "Аудит" не выполняет никаких действий по регулированию в процессе аудита.</span><span class="sxs-lookup"><span data-stu-id="70b0d-166">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="70b0d-167">Вместо этого оно просто экстраполяция того, сколько времени займет загрузка страницы в условиях мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="70b0d-167">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="70b0d-168">Параметр " **применено...** ", в свою очередь, в действительности регулирует производительность процессора и сети с компромиссом более продолжительного процесса аудита.</span><span class="sxs-lookup"><span data-stu-id="70b0d-168">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="70b0d-169">**Очистите хранилище**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-169">**Clear Storage**.</span></span>  <span data-ttu-id="70b0d-170">При установке этого флажка все хранилище, связанное со страницей, будет очищено перед каждым аудитом.</span><span class="sxs-lookup"><span data-stu-id="70b0d-170">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="70b0d-171">Оставьте этот параметр, если вы хотите подвергать аудиту, как посетители в первый раз будут работать на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="70b0d-171">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="70b0d-172">Отключите этот параметр, если вы хотите использовать функцию повторного посещения.</span><span class="sxs-lookup"><span data-stu-id="70b0d-172">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="70b0d-173">Нажмите кнопку **запустить аудиты**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-173">Select **Run Audits**.</span></span>  <span data-ttu-id="70b0d-174">После 10 – 30 секунд на панели «аудиты» отображается отчет о быстродействии сайта.</span><span class="sxs-lookup"><span data-stu-id="70b0d-174">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Отчет для панели «аудит» для производительности сайта" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="70b0d-176">Отчет для панели «аудит» для производительности сайта</span><span class="sxs-lookup"><span data-stu-id="70b0d-176">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="70b0d-177">Обработка ошибок отчета</span><span class="sxs-lookup"><span data-stu-id="70b0d-177">Handling report errors</span></span>   

<span data-ttu-id="70b0d-178">Если вы когда-либо получаете сообщение об ошибке в отчете на панели аудиты, попробуйте запустить вкладку Demo из окна **InPrivate** без открытия других вкладок.</span><span class="sxs-lookup"><span data-stu-id="70b0d-178">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="70b0d-179">Это гарантирует, что вы используете Microsoft Edge из чистого состояния.</span><span class="sxs-lookup"><span data-stu-id="70b0d-179">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="70b0d-180">Определенные расширения Microsoft Edge часто мешают процессу аудита.</span><span class="sxs-lookup"><span data-stu-id="70b0d-180">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="70b0d-181">Понимание отчета</span><span class="sxs-lookup"><span data-stu-id="70b0d-181">Understand your report</span></span>   

<span data-ttu-id="70b0d-182">Число в верхней части отчета является общим показателем эффективности сайта.</span><span class="sxs-lookup"><span data-stu-id="70b0d-182">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="70b0d-183">После внесения изменений в код вы должны увидеть этот номер.</span><span class="sxs-lookup"><span data-stu-id="70b0d-183">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="70b0d-184">Более высокие баллы означают более высокую производительность.</span><span class="sxs-lookup"><span data-stu-id="70b0d-184">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Общая оценка производительности" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="70b0d-186">Общая оценка производительности</span><span class="sxs-lookup"><span data-stu-id="70b0d-186">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-187">Раздел **метрики** содержит количественные измерения производительности сайта.</span><span class="sxs-lookup"><span data-stu-id="70b0d-187">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="70b0d-188">Каждая метрика обеспечивает различные аспекты производительности.</span><span class="sxs-lookup"><span data-stu-id="70b0d-188">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="70b0d-189">Например, при первом обобщении с **содержимым** появляется сообщение о том, что содержимое сначала закрашено на экран, что является важной вехой в восприятии загрузки страницы, в то время как в **интерактивном режиме** отмечается тот момент, когда страница будет готова для обработки взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="70b0d-189">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Раздел метрики" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="70b0d-191">Раздел **метрики**</span><span class="sxs-lookup"><span data-stu-id="70b0d-191">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-192">Щелкните выделенный выключатель на приведенном ниже рисунке, чтобы просмотреть описание каждой метрики, а затем нажмите Дополнительные **сведения** , чтобы прочитать его документацию.</span><span class="sxs-lookup"><span data-stu-id="70b0d-192">Select the highlighted toggle button in the following figure to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Щелкните выделенный выключатель, чтобы развернуть элементы метрик" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="70b0d-194">Щелкните выделенный выключатель, чтобы развернуть элементы метрик</span><span class="sxs-lookup"><span data-stu-id="70b0d-194">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-195">Под метриками представлен набор снимков экрана, показывающий, как страница выглядит как загруженная.</span><span class="sxs-lookup"><span data-stu-id="70b0d-195">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Снимки экрана, посвященные загрузке страницы" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="70b0d-197">Снимки экрана, посвященные загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="70b0d-197">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-198">В разделе " **возможности** " представлены конкретные советы по повышению производительности загрузки данной страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-198">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Раздел "возможности"" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="70b0d-200">Раздел " **возможности** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-200">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-201">Выберите возможность, чтобы узнать больше о ней.</span><span class="sxs-lookup"><span data-stu-id="70b0d-201">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Исключение ресурсов блокировки рендеринга возможная сделка" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="70b0d-203">**Исключение ресурсов блокировки рендеринга** возможная сделка</span><span class="sxs-lookup"><span data-stu-id="70b0d-203">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-204">Выберите дополнительные **сведения** , чтобы ознакомиться с документацией о важности возможной сделки, и конкретные рекомендации по ее устранению.</span><span class="sxs-lookup"><span data-stu-id="70b0d-204">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Документация по устранению ресурсов с блокировкой рендеринга возможная сделка" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="70b0d-206">Документация по **устранению ресурсов с блокировкой рендеринга** возможная сделка</span><span class="sxs-lookup"><span data-stu-id="70b0d-206">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-207">Раздел **Диагностика** содержит дополнительные сведения о факторах, которые влияют на время загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-207">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Раздел "Диагностика"" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="70b0d-209">Раздел " **Диагностика** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-209">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-210">В разделе **переданные аудиты** показано, что делает сайт правильно.</span><span class="sxs-lookup"><span data-stu-id="70b0d-210">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="70b0d-211">Выберите этот пункт, чтобы развернуть раздел.</span><span class="sxs-lookup"><span data-stu-id="70b0d-211">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Раздел "пройденные аудиты"" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="70b0d-213">Раздел " **пройденные аудиты** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-213">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="70b0d-214">Этап 2: эксперименты</span><span class="sxs-lookup"><span data-stu-id="70b0d-214">Step 2: Experiment</span></span>   

<span data-ttu-id="70b0d-215">Раздел "возможности" в отчете об аудите содержит советы по улучшению производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-215">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="70b0d-216">В этом разделе вы реализуете рекомендованные изменения в базе кода, проведя аудит сайта после каждого изменения, чтобы определить, как оно влияет на скорость сайта.</span><span class="sxs-lookup"><span data-stu-id="70b0d-216">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="70b0d-217">Включение сжатия текста</span><span class="sxs-lookup"><span data-stu-id="70b0d-217">Enable text compression</span></span>   

<span data-ttu-id="70b0d-218">В отчете говорится, что отсутствие огромных полезных данных сети является одной из самых первых возможностей для повышения производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-218">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="70b0d-219">Включить сжатие текста — это возможность улучшить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-219">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="70b0d-220">Сжатие текста — это сокращение размера текстового файла перед отправкой по сети, а также его сжатие.</span><span class="sxs-lookup"><span data-stu-id="70b0d-220">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="70b0d-221">Например, вы можете почтовые индексы, чтобы уменьшить размер папки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-221">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="70b0d-222">Перед включением сжатия вы можете вручную проверить, сжимаются ли текстовые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-222">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="70b0d-223">Откройте вкладку **сеть** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-223">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Панель "сеть"" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="70b0d-225">Панель " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-225">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-226">Выберите значок **Параметры сети** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-226">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="70b0d-227">Установите флажок **использовать строки большого запроса** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-227">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="70b0d-228">Высота строк в таблице сетевых запросов возрастает.</span><span class="sxs-lookup"><span data-stu-id="70b0d-228">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Большие строки в таблице "сетевые запросы"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="70b0d-230">Большие строки в таблице "сетевые запросы"</span><span class="sxs-lookup"><span data-stu-id="70b0d-230">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-231">Если столбец **Размер** не отображается в таблице сетевых запросов, щелкните заголовок таблицы и выберите команду **Размер**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-231">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="70b0d-232">В каждой ячейке **размера** отображаются два значения.</span><span class="sxs-lookup"><span data-stu-id="70b0d-232">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="70b0d-233">Верхнее значение — размер загруженного ресурса.</span><span class="sxs-lookup"><span data-stu-id="70b0d-233">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="70b0d-234">Минимальное значение — размер несжатого ресурса.</span><span class="sxs-lookup"><span data-stu-id="70b0d-234">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="70b0d-235">Если оба значения совпадают, значит, ресурс не сжимается, когда он отправляется по сети.</span><span class="sxs-lookup"><span data-stu-id="70b0d-235">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="70b0d-236">Например, на предыдущем рисунке значения Top и Bottom для параметров "" `bundle.js` — " `1.2 MB` и" `1.2 MB` ... ".</span><span class="sxs-lookup"><span data-stu-id="70b0d-236">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="70b0d-237">Проверка на наличие сжатия с помощью проверки заголовков HTTP ресурса.</span><span class="sxs-lookup"><span data-stu-id="70b0d-237">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="70b0d-238">Выберите **bundle.js**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-238">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="70b0d-239">Откройте вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-239">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Вкладка "заголовки"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="70b0d-241">Вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-241">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-242">Поиск заголовка в разделе **заголовков ответа** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-242">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="70b0d-243">Вы не видите один из них, то есть `bundle.js` не был сжат.</span><span class="sxs-lookup"><span data-stu-id="70b0d-243">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="70b0d-244">Когда ресурс сжимается, этот верхний колонтитул обычно имеет значение `gzip` , `deflate` или `br` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-244">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="70b0d-245">Описание этих значений показано в разделе [директивы][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="70b0d-245">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="70b0d-246">Достаточно с пояснениями.</span><span class="sxs-lookup"><span data-stu-id="70b0d-246">Enough with the explanations.</span></span>  <span data-ttu-id="70b0d-247">Время, чтобы внести некоторые изменения!</span><span class="sxs-lookup"><span data-stu-id="70b0d-247">Time to make some changes!</span></span>  <span data-ttu-id="70b0d-248">Включите сжатие текста, добавив несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="70b0d-248">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="70b0d-249">На вкладке "редактор" нажмите кнопку " **server.js**".</span><span class="sxs-lookup"><span data-stu-id="70b0d-249">In the editor tab, click **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Изменить server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="70b0d-251">Edit</span><span class="sxs-lookup"><span data-stu-id="70b0d-251">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-252">Добавьте следующий код для **server.js**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-252">Add the following code to **server.js**.</span></span>  <span data-ttu-id="70b0d-253">Убедитесь, что он должен быть помещен `app.use(compression())` `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-253">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="70b0d-254">Как правило, вы должны установить `compression` пакет с помощью какого-либо вида `npm i -S compression` , но это еще не сделано.</span><span class="sxs-lookup"><span data-stu-id="70b0d-254">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="70b0d-255">Дождитесь, пока не будет развернуто новая сборка сайта.</span><span class="sxs-lookup"><span data-stu-id="70b0d-255">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="70b0d-256">Неузорная анимация рядом с **инструментами** означает, что сайт перестраивается и повторно развертывается.</span><span class="sxs-lookup"><span data-stu-id="70b0d-256">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="70b0d-257">Изменение будет готово, когда анимация рядом с пунктом " **инструменты** " исчезает.</span><span class="sxs-lookup"><span data-stu-id="70b0d-257">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="70b0d-258">Нажмите кнопку **Показать** и выберите **в новом окне** еще раз.</span><span class="sxs-lookup"><span data-stu-id="70b0d-258">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="70b0d-259">Используйте рабочие процессы, которые вы узнали ранее, чтобы вручную проверить, работает ли сжатие.</span><span class="sxs-lookup"><span data-stu-id="70b0d-259">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="70b0d-260">Вернитесь на вкладку Demo и повторно загрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="70b0d-260">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="70b0d-261">Столбец « **Размер** » теперь должен показывать 2 разных значения для текстовых ресурсов `bundle.js` , таких как.</span><span class="sxs-lookup"><span data-stu-id="70b0d-261">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="70b0d-262">На рисунке после следующего значения аргумента " `256 KB` `bundle.js` равно" — Размер файла, отправленного по сети, а в качестве нижнего значения `1.2 MB` — несжатый размер файла.</span><span class="sxs-lookup"><span data-stu-id="70b0d-262">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="В столбце "размер" теперь показано 2 разных значения для текстовых ресурсов." lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="70b0d-264">В столбце " **Размер** " теперь показано 2 разных значения для текстовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70b0d-264">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-265">В разделе **заголовки ответа** `bundle.js` теперь должен быть указан `content-encoding: gzip` верхний колонтитул.</span><span class="sxs-lookup"><span data-stu-id="70b0d-265">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Раздел заголовки ответа теперь содержат заголовок Content-Encoding" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="70b0d-267">Раздел **заголовки ответа** теперь содержат заголовок Content-Encoding</span><span class="sxs-lookup"><span data-stu-id="70b0d-267">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70b0d-268">Проведите аудит страницы, чтобы оценить, какое влияние сжатие текста влияет на производительность загрузки страницы:</span><span class="sxs-lookup"><span data-stu-id="70b0d-268">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="70b0d-269">Перейдите на вкладку **Аудит** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-269">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="70b0d-270">Выберите **выполнить аудит** \ ( ![ выполнить аудит ][ImagePerformIcon] ).</span><span class="sxs-lookup"><span data-stu-id="70b0d-270">Select **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="70b0d-271">Параметры не совпадают.</span><span class="sxs-lookup"><span data-stu-id="70b0d-271">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="70b0d-272">Нажмите кнопку **запустить аудит**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-272">Select **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Отчет "Аудит" после включения сжатия текста" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="70b0d-274">Отчет "Аудит" после включения сжатия текста</span><span class="sxs-lookup"><span data-stu-id="70b0d-274">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="70b0d-275">Общая оценка производительности должна быть увеличена, а это значит, что сайт быстрее.</span><span class="sxs-lookup"><span data-stu-id="70b0d-275">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="70b0d-276">Сжатие текста в реальном мире</span><span class="sxs-lookup"><span data-stu-id="70b0d-276">Text compression in the real world</span></span>   

<span data-ttu-id="70b0d-277">На большинстве серверов есть простые решения, подобные этим, чтобы включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="70b0d-277">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="70b0d-278">Просто выполните поиск, чтобы настроить любой сервер, который вы используете для сжатия текста.</span><span class="sxs-lookup"><span data-stu-id="70b0d-278">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="70b0d-279">Изменение размера изображения</span><span class="sxs-lookup"><span data-stu-id="70b0d-279">Resize images</span></span>   

<span data-ttu-id="70b0d-280">Отчет о том, что не следует избегать огромных полезных данных сети, является одной из самых первых возможностей для повышения производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-280">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="70b0d-281">Изменение размеров изображений помогает уменьшить размер полезных данных в сети.</span><span class="sxs-lookup"><span data-stu-id="70b0d-281">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="70b0d-282">Если пользователь просматривает изображения на экране мобильного устройства размером 500 в пикселах, это не значит, что при отправке изображения в масштабе не более 1500 точек.</span><span class="sxs-lookup"><span data-stu-id="70b0d-282">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="70b0d-283">В идеале вы отправляете изображение в 500 в масштабе по пикселю.</span><span class="sxs-lookup"><span data-stu-id="70b0d-283">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="70b0d-284">В отчете выберите команду **Избегайте огромных полезных данных сети** , чтобы узнать, какие изображения нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="70b0d-284">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="70b0d-285">Похоже, что 2 файлов JPG — более 2000 КБ, что больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="70b0d-285">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="70b0d-286">Вернувшись на вкладку Редактор, открыть `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-286">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="70b0d-287">Заменить `const dir = 'big'` на `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-287">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="70b0d-288">Этот каталог содержит копии тех же изображений, размер которых был изменен.</span><span class="sxs-lookup"><span data-stu-id="70b0d-288">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="70b0d-289">Вновь проведите аудит страницы, чтобы увидеть, как это изменение влияет на производительность загрузки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-289">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Отчет об аудите после изменения размеров изображений" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="70b0d-291">Отчет об аудите после изменения размеров изображений</span><span class="sxs-lookup"><span data-stu-id="70b0d-291">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70b0d-292">Похоже, что изменение имеет незначительный уровень влияния на общую оценку производительности.</span><span class="sxs-lookup"><span data-stu-id="70b0d-292">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="70b0d-293">Тем не менее, в этом случае баллы не показываются четко, так как данные сети, которые вы сохраняете, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="70b0d-293">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="70b0d-294">Общий размер старой фотографии — около 5,3 мегабайт, в то время как теперь это не более 0,18 МБ.</span><span class="sxs-lookup"><span data-stu-id="70b0d-294">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="70b0d-295">Изменение размеров изображений в реальном мире</span><span class="sxs-lookup"><span data-stu-id="70b0d-295">Resizing images in the real world</span></span>   

<span data-ttu-id="70b0d-296">В случае с небольшим приложением вы можете использовать один из этих способов, так как это может быть достаточно хорошим.</span><span class="sxs-lookup"><span data-stu-id="70b0d-296">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="70b0d-297">Но для больших приложений это очевидно не масштабируется.</span><span class="sxs-lookup"><span data-stu-id="70b0d-297">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="70b0d-298">Ниже приведены некоторые стратегии управления изображениями в крупных приложениях.</span><span class="sxs-lookup"><span data-stu-id="70b0d-298">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="70b0d-299">Изменение размера изображения во время процесса сборки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-299">Resize images during your build process.</span></span>  
*   <span data-ttu-id="70b0d-300">Создавайте несколько размеров изображения во время процесса сборки, а затем используйте `srcset` их в коде.</span><span class="sxs-lookup"><span data-stu-id="70b0d-300">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="70b0d-301">Во время выполнения браузер берет на себя выбор оптимального размера для устройства.</span><span class="sxs-lookup"><span data-stu-id="70b0d-301">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="70b0d-302">Использование сети CDN изображений, позволяющей динамически изменять размер изображения при запросе.</span><span class="sxs-lookup"><span data-stu-id="70b0d-302">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="70b0d-303">По крайней мере, оптимизируйте каждое изображение.</span><span class="sxs-lookup"><span data-stu-id="70b0d-303">At the very least, optimize each image.</span></span>  <span data-ttu-id="70b0d-304">Это может создать огромный выигрыш.</span><span class="sxs-lookup"><span data-stu-id="70b0d-304">This may create huge savings.</span></span>  
  <span data-ttu-id="70b0d-305">Оптимизация — это время, когда вы запускаете изображение с помощью специальной программы, которая уменьшает размер файла изображения.</span><span class="sxs-lookup"><span data-stu-id="70b0d-305">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="70b0d-306">Дополнительные советы приведены в статье основные сведения об [оптимизации изображений][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="70b0d-306">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="70b0d-307">Исключение ресурсов блокировки рендеринга</span><span class="sxs-lookup"><span data-stu-id="70b0d-307">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="70b0d-308">В последней версии отчета говорится о том, что в настоящее время ресурсы, блокирующие рендеринг, стали самой большой возможностью.</span><span class="sxs-lookup"><span data-stu-id="70b0d-308">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="70b0d-309">Ресурс блокировки обработки — это внешний файл JavaScript или CSS, который браузер должен загрузить, проанализировать и выполнить, прежде чем отобразить страницу.</span><span class="sxs-lookup"><span data-stu-id="70b0d-309">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="70b0d-310">Цель состоит в том, чтобы запустить только основной код CSS и JavaScript, необходимый для правильного отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-310">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="70b0d-311">Первая задача — это поиск кода, который не нужно выполнять при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-311">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="70b0d-312">Чтобы просмотреть блокируемые ресурсы, выберите пункт **удалить ресурсы блокировки рендеринга** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-312">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="70b0d-313">и `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-313">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Дополнительные сведения о ресурсах блокировки обработки с возможностью устранения" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="70b0d-315">Дополнительные сведения о **ресурсах блокировки обработки** с возможностью устранения</span><span class="sxs-lookup"><span data-stu-id="70b0d-315">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-316">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, начните вводить текст `Coverage` и выберите пункт **Показать покрытие**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-316">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Открытие меню "команд" на панели "Аудит"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="70b0d-318">Открытие меню "команд" на панели " **Аудит** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-318">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Вкладка "покрытие"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="70b0d-320">Вкладка " **покрытие** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-320">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-321">Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="70b0d-321">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="70b0d-322">На вкладке " **покрытие** " представлены общие сведения о том, какая часть `bundle.js` кода `jquery.js` и `lodash.js` выполняется при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-322">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="70b0d-323">На рисунке ниже показано, что около 76% и 30% файлов jQuery и Lodash не используются соответственно.</span><span class="sxs-lookup"><span data-stu-id="70b0d-323">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Отчет о покрытии" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="70b0d-325">Отчет о покрытии</span><span class="sxs-lookup"><span data-stu-id="70b0d-325">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-326">Выделите строку **jquery.js** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-326">Select the **jquery.js** row.</span></span>  <span data-ttu-id="70b0d-327">DevTools откроет файл на панели «источники».</span><span class="sxs-lookup"><span data-stu-id="70b0d-327">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="70b0d-328">Строка кода была выполнена, если рядом с ней есть синяя полоска.</span><span class="sxs-lookup"><span data-stu-id="70b0d-328">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="70b0d-329">Красная черта означает, что она не была выполнена и определенно не требуется при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-329">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Просмотр файла jQuery на панели «источники»" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="70b0d-331">Просмотр файла jQuery на панели « **источники** »</span><span class="sxs-lookup"><span data-stu-id="70b0d-331">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-332">Прокрутите код jQuery на немного.</span><span class="sxs-lookup"><span data-stu-id="70b0d-332">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="70b0d-333">Некоторые строки, которые получают слово "выполнить", на самом деле представляют собой комментарии.</span><span class="sxs-lookup"><span data-stu-id="70b0d-333">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="70b0d-334">Выполнение этого кода с помощью Minifier, который содержит примечания, — еще один способ уменьшить размер файла.</span><span class="sxs-lookup"><span data-stu-id="70b0d-334">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="70b0d-335">Коротко говоря, при работе с собственным кодом вкладка "покрытие" помогает проанализировать код, построчно и поставлять только код, необходимый для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-335">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="70b0d-336">Нужны ли `jquery.js` `lodash.js` файлы и даже для загрузки страницы?</span><span class="sxs-lookup"><span data-stu-id="70b0d-336">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="70b0d-337">На вкладке Блокировка запроса показано, что происходит, когда ресурсы недоступны.</span><span class="sxs-lookup"><span data-stu-id="70b0d-337">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="70b0d-338">Откройте вкладку **сеть** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-338">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="70b0d-339">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы снова открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="70b0d-339">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="70b0d-340">Начните вводить данные `blocking` и установите флажок **Показать блокировку запросов**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-340">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Вкладка "блокировка запросов"" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="70b0d-342">Вкладка " **Блокировка запросов** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-342">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-343">Нажмите кнопку **Добавить узор** \ ( ![ Добавить шаблон ][ImageAddPatternIcon] \), введите текст и нажмите `/libs/*` кнопку, `Enter` чтобы подтвердить.</span><span class="sxs-lookup"><span data-stu-id="70b0d-343">Select **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Добавление шаблона для блокирования запросов в каталог библиотек" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="70b0d-345">Добавление шаблона для блокирования запросов в `libs` Каталог</span><span class="sxs-lookup"><span data-stu-id="70b0d-345">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-346">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="70b0d-346">Refresh the page.</span></span>  <span data-ttu-id="70b0d-347">Запросы jQuery и Lodash красного цвета, означающие, что запросы были заблокированы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-347">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="70b0d-348">Страница по-прежнему загружается и является интерактивной, поэтому она выглядит так, как это не требуется.</span><span class="sxs-lookup"><span data-stu-id="70b0d-348">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="На панели Network (сеть) показано, что запросы заблокированы" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="70b0d-350">На панели **Network (сеть** ) показано, что запросы заблокированы</span><span class="sxs-lookup"><span data-stu-id="70b0d-350">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-351">Выберите команду **удалить все шаблоны** \ ( ![ удалить все шаблоны ][ImageRemoveIcon] \), чтобы удалить `/libs/*` шаблон блокировки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-351">Select **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="70b0d-352">Как правило, вкладка "блокировка запросов" полезна для имитации того, как работает страница, если какой-либо из указанных ресурсов недоступен.</span><span class="sxs-lookup"><span data-stu-id="70b0d-352">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="70b0d-353">Теперь удалите ссылки на эти файлы из кода и выполните аудит страницы еще раз:</span><span class="sxs-lookup"><span data-stu-id="70b0d-353">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="70b0d-354">Вернувшись на вкладку Редактор, открыть `template.html` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-354">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="70b0d-355">Удалите `<script src="/libs/lodash.js">` и `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="70b0d-355">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="70b0d-356">Дождитесь повторного создания и повторного развертывания сайта.</span><span class="sxs-lookup"><span data-stu-id="70b0d-356">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="70b0d-357">Снова проведите аудит страницы с помощью панели **аудита** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-357">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="70b0d-358">Ваши общие баллы должны быть улучшены.</span><span class="sxs-lookup"><span data-stu-id="70b0d-358">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Отчет об аудите после удаления ресурсов блокировки рендеринга" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="70b0d-360">Отчет об **аудите** после удаления ресурсов блокировки рендеринга</span><span class="sxs-lookup"><span data-stu-id="70b0d-360">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="70b0d-361">Оптимизация критического пути отрисовки в реальном мире</span><span class="sxs-lookup"><span data-stu-id="70b0d-361">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="70b0d-362">**Критический путь рендеринга** указывает на код, необходимый для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-362">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="70b0d-363">Как правило, скорость загрузки страницы повышается за счет отправки критического кода только при загрузке страницы, а затем — через отложенную загрузку всех остальных.</span><span class="sxs-lookup"><span data-stu-id="70b0d-363">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="70b0d-364">Маловероятно, что вы можете найти сценарии, которые можно удалить прямо, но вы можете найти большое количество сценариев, которые вам не нужно запрашивать во время загрузки страницы, и, возможно, они будут запрашиваться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="70b0d-364">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="70b0d-365">Если вы используете платформу, убедитесь в том, что у нее есть производственный режим.</span><span class="sxs-lookup"><span data-stu-id="70b0d-365">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="70b0d-366">Этот режим может использовать такие функции, как [Tree встряхнув][WebpackTreeShaking] , для удаления ненужного кода, блокирующего критический рендеринг.</span><span class="sxs-lookup"><span data-stu-id="70b0d-366">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="70b0d-367">Работа менее основного потока</span><span class="sxs-lookup"><span data-stu-id="70b0d-367">Do less main thread work</span></span>   

<span data-ttu-id="70b0d-368">В последней версии отчета представлены некоторые небольшие возможности по экономии средств в разделе "возможности", но если вы просмотрии раздел "Диагностика", это похоже на то, что наибольший узкий участок слишком велик для основного потока.</span><span class="sxs-lookup"><span data-stu-id="70b0d-368">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="70b0d-369">Основной поток — это тот случай, когда браузер выполняет большую часть работы, необходимой для отображения страницы, например синтаксического анализа и выполнения HTML, CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="70b0d-369">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="70b0d-370">Цель состоит в том, чтобы проанализировать трудозатраты, выполняемые основным потоком при загрузке страницы, и найти способы задержать или удалить ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="70b0d-370">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="70b0d-371">Откройте вкладку **производительность** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-371">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="70b0d-372">Выберите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureIcon] ).</span><span class="sxs-lookup"><span data-stu-id="70b0d-372">Select **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="70b0d-373">Настройте **сеть** на **медленное 3G** и **ЦП** , чтобы **6X замедление**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-373">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="70b0d-374">На мобильных устройствах обычно используются больше ограничений на оборудование, чем на ноутбуках или настольных компьютерах, поэтому эти параметры позволяют загрузить страницу так, как если бы вы использовали менее мощное устройство.</span><span class="sxs-lookup"><span data-stu-id="70b0d-374">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="70b0d-375">Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="70b0d-375">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="70b0d-376">DevTools обновляет страницу и создает визуализацию всей выполненной работы, чтобы загрузить страницу.</span><span class="sxs-lookup"><span data-stu-id="70b0d-376">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="70b0d-377">Этот зрительный образ называется **трассировкой**.</span><span class="sxs-lookup"><span data-stu-id="70b0d-377">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Трассировка загрузки страницы на панели производительности" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="70b0d-379">Трассировка загрузки страницы на панели **производительности**</span><span class="sxs-lookup"><span data-stu-id="70b0d-379">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70b0d-380">Трассировка отображает операцию в хронологическом порядке, слева направо.</span><span class="sxs-lookup"><span data-stu-id="70b0d-380">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="70b0d-381">На диаграммах с частотой кадров, ЦП и нетто в верхней части экрана дается обзор кадров в секунду, активности ЦП и активности сети.</span><span class="sxs-lookup"><span data-stu-id="70b0d-381">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="70b0d-382">Выделенный блок желтого цвета, показанный на рисунке после следующего, ЦП полностью загружен с действиями в сценарии.</span><span class="sxs-lookup"><span data-stu-id="70b0d-382">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="70b0d-383">Это говорит о том, что вы можете ускорить загрузку страницы, выполнив меньше действий JavaScript.</span><span class="sxs-lookup"><span data-stu-id="70b0d-383">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Раздел обзора трассировки" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="70b0d-385">Раздел обзора трассировки</span><span class="sxs-lookup"><span data-stu-id="70b0d-385">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="70b0d-386">Изучите трассировку, чтобы найти способы выполнения меньшей работы в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="70b0d-386">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="70b0d-387">Щелкните раздел **время показа** , чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="70b0d-387">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="70b0d-388">В зависимости от того факта, что существует ряд мер [времени][MDNUserTimingApi] , не отклика, может показаться, что приложение Илья использует режим разработки реагируй.</span><span class="sxs-lookup"><span data-stu-id="70b0d-388">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="70b0d-389">Переключение в режим рабочего режима может привести к снижению производительности WINS.</span><span class="sxs-lookup"><span data-stu-id="70b0d-389">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Раздел "временные интервалы"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="70b0d-391">Раздел " **временные интервалы** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-391">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-392">Чтобы свернуть этот раздел, выберите пункт **время показа** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-392">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="70b0d-393">Просмотрите **основной** раздел.</span><span class="sxs-lookup"><span data-stu-id="70b0d-393">Browse the **Main** section.</span></span>  <span data-ttu-id="70b0d-394">В этом разделе показан хронологический журнал основных операций потока, слева направо.</span><span class="sxs-lookup"><span data-stu-id="70b0d-394">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="70b0d-395">Ось y (сверху вниз) показывает причины возникновения событий.</span><span class="sxs-lookup"><span data-stu-id="70b0d-395">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="70b0d-396">Например, в figyre после указанных ниже `Evaluate Script` событий событие привело `(anonymous)` к выполнению функции, которое привело к выполнению `(anonymous)` `__webpack__require__` и т. д.</span><span class="sxs-lookup"><span data-stu-id="70b0d-396">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Основной раздел" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="70b0d-398">**Основной** раздел</span><span class="sxs-lookup"><span data-stu-id="70b0d-398">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70b0d-399">Прокрутите страницу вниз до конца **основного** раздела.</span><span class="sxs-lookup"><span data-stu-id="70b0d-399">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="70b0d-400">При использовании платформы большая часть верхнего действия вызывается платформой, которая обычно находится в вашем элементе управления.</span><span class="sxs-lookup"><span data-stu-id="70b0d-400">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="70b0d-401">Действия, вызванные вашим приложением, обычно находятся в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="70b0d-401">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="70b0d-402">В этом приложении это похоже на функцию с именем, которая `App` вызывает большое количество запросов к `mineBitcoin` функции.</span><span class="sxs-lookup"><span data-stu-id="70b0d-402">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="70b0d-403">Это звучит так, как Илья может использовать устройства своего вентилятора для cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="70b0d-403">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Наведите указатель мыши на действие mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="70b0d-405">Наведение указателя на `mineBitcoin` мероприятие</span><span class="sxs-lookup"><span data-stu-id="70b0d-405">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="70b0d-406">Несмотря на то что запросы вашей платформы обычно прерываются из вашего элемента управления, иногда вы можете структурировать приложение таким образом, чтобы она выполнялась неэффективно.</span><span class="sxs-lookup"><span data-stu-id="70b0d-406">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="70b0d-407">Реструктуризация приложения для эффективного использования инфраструктуры — это способ выполнения менее основного потока работ.</span><span class="sxs-lookup"><span data-stu-id="70b0d-407">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="70b0d-408">Тем не менее, для этого необходимо глубокое понимание того, как работает ваша платформа, и какие изменения вносятся в вашем собственном коде для более эффективной работы с платформой.</span><span class="sxs-lookup"><span data-stu-id="70b0d-408">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="70b0d-409">Разверните раздел **снизу вверх** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-409">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="70b0d-410">На этой вкладке прерываются действия, которые выполнялись в течение всего времени.</span><span class="sxs-lookup"><span data-stu-id="70b0d-410">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="70b0d-411">Если в разделе снизу вверх ничего не видно, щелкните надпись для **основного** раздела.</span><span class="sxs-lookup"><span data-stu-id="70b0d-411">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="70b0d-412">В разделе " **снизу вверх** " отображаются только сведения о каких-либо действиях или группах действий, которые вы уже выбрали.</span><span class="sxs-lookup"><span data-stu-id="70b0d-412">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="70b0d-413">Например, если вы `mineBitcoin` **настроили** одно из действий, в разделе снизу вверх будет отображаться только информация для этого действия.</span><span class="sxs-lookup"><span data-stu-id="70b0d-413">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Вкладка "снизу вверх"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="70b0d-415">Вкладка " **снизу вверх** "</span><span class="sxs-lookup"><span data-stu-id="70b0d-415">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70b0d-416">В столбце " **собственное время** " показано, сколько времени было затрачено непосредственно на каждое действие.</span><span class="sxs-lookup"><span data-stu-id="70b0d-416">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="70b0d-417">Например, на приведенном ниже рисунке около 63% времени основного потока было затрачено на выполнение `mineBitcoin` функции.</span><span class="sxs-lookup"><span data-stu-id="70b0d-417">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="70b0d-418">Время от времени до того, чтобы узнать, используется ли производственный режим и уменьшается активность JavaScript, может ускорить загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-418">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="70b0d-419">Начните работу в режиме "в производство":</span><span class="sxs-lookup"><span data-stu-id="70b0d-419">Start with production mode:</span></span>  

1.  <span data-ttu-id="70b0d-420">На вкладке Редактор откройте `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-420">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="70b0d-421">Заменить `"mode":"development"` на `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-421">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="70b0d-422">Дождитесь завершения развертывания новой сборки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-422">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="70b0d-423">Вновь проведите аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-423">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Отчет по аудиту после настройки пакета для использования режима "в производство"" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="70b0d-425">Отчет по аудиту после настройки пакета для использования режима "в производство"</span><span class="sxs-lookup"><span data-stu-id="70b0d-425">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70b0d-426">Сокращение действий JavaScript путем удаления запроса на `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="70b0d-426">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="70b0d-427">На вкладке Редактор откройте `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-427">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="70b0d-428">Закомментируйте запрос `this.mineBitcoin(1500)` в `constructor` .</span><span class="sxs-lookup"><span data-stu-id="70b0d-428">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="70b0d-429">Дождитесь завершения развертывания новой сборки.</span><span class="sxs-lookup"><span data-stu-id="70b0d-429">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="70b0d-430">Вновь проведите аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="70b0d-430">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Отчет по аудиту после удаления ненужных действий JavaScript" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="70b0d-432">Отчет по аудиту после удаления ненужных действий JavaScript</span><span class="sxs-lookup"><span data-stu-id="70b0d-432">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70b0d-433">Похоже, что Последнее изменение вызвало значительный переход в производительности!</span><span class="sxs-lookup"><span data-stu-id="70b0d-433">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="70b0d-434">Этот раздел предоставил краткое введение в панель производительности.</span><span class="sxs-lookup"><span data-stu-id="70b0d-434">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="70b0d-435">Дополнительные сведения о том, как анализировать производительность страниц, можно найти в статье [Анализ производительности][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="70b0d-435">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="70b0d-436">Выполнение менее основного потока работ в реальном мире</span><span class="sxs-lookup"><span data-stu-id="70b0d-436">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="70b0d-437">Как правило, панель **производительности** является наиболее распространенным способом для понимания того, какие действия выполняет загружаемый сайт, и Узнайте о способах удаления ненужных действий.</span><span class="sxs-lookup"><span data-stu-id="70b0d-437">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="70b0d-438">Если вы предпочитаете использовать более похожий подход `console.log()` , Пользовательский API для работы с [временными][MDNUserTimingApi] сведениями позволяет вам произвольно помечать определенные этапы жизненного цикла приложения, чтобы отслеживать продолжительность каждого из этих фаз.</span><span class="sxs-lookup"><span data-stu-id="70b0d-438">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="70b0d-439">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="70b0d-439">Summary</span></span>   

*   <span data-ttu-id="70b0d-440">Каждый раз, когда вы задаете оптимальное качество нагрузки для сайта, всегда начинайте с аудита.</span><span class="sxs-lookup"><span data-stu-id="70b0d-440">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="70b0d-441">Аудит определяет базовые показатели и предоставляет советы по улучшению.</span><span class="sxs-lookup"><span data-stu-id="70b0d-441">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="70b0d-442">За один раз сделайте одно изменение и проведите аудит страницы после каждого изменения, чтобы увидеть, как это изолированное изменение влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="70b0d-442">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Справка по анализу производительности | Документы Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Знакомство с классом веб-разработки | Coursera"  

[EssentialImageOptimization]: https://images.guide "Оптимизация изображений"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Директивы-кодировка содержимого | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API времени пользователя | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Tree встряхнув | упаковать"  

> [!NOTE]
> <span data-ttu-id="70b0d-449">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="70b0d-449">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="70b0d-450">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="70b0d-450">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="70b0d-452">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="70b0d-452">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

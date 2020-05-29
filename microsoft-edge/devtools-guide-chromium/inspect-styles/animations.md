---
title: Проверка анимации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572411"
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





# <span data-ttu-id="47c46-103">Проверка анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-103">Inspect animations</span></span>   



<span data-ttu-id="47c46-104">Просмотрите и измените анимацию с помощью инспектора анимации Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="47c46-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

> ##### <span data-ttu-id="47c46-105">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="47c46-105">Figure 1</span></span>  
> <span data-ttu-id="47c46-106">Инспектор анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-106">Animation inspector</span></span>  
> ![Инспектор анимации][ImageAnimationInspector]  

### <span data-ttu-id="47c46-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="47c46-108">Summary</span></span>  

*   <span data-ttu-id="47c46-109">Запишите анимацию, открыв инспектор анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="47c46-110">Инспектор анимации автоматически определяет и сортирует анимации в группах.</span><span class="sxs-lookup"><span data-stu-id="47c46-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="47c46-111">Изучите анимацию, заменив каждую из них, воспроизводить каждую из них или просматривая исходный код.</span><span class="sxs-lookup"><span data-stu-id="47c46-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="47c46-112">Изменяйте анимацию, изменяя время, задержку, продолжительность или смещение опорных кадров.</span><span class="sxs-lookup"><span data-stu-id="47c46-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="47c46-113">Обзор</span><span class="sxs-lookup"><span data-stu-id="47c46-113">Overview</span></span>   

<span data-ttu-id="47c46-114">Инспектор анимации Microsoft Edge DevTools имеет два основных назначения.</span><span class="sxs-lookup"><span data-stu-id="47c46-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="47c46-115">Проверка анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-115">Inspecting animations.</span></span>  <span data-ttu-id="47c46-116">Вы хотите замедлить, воспроизвести или проверить исходный код для группы анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="47c46-117">Изменение анимаций.</span><span class="sxs-lookup"><span data-stu-id="47c46-117">Modifying animations.</span></span>  <span data-ttu-id="47c46-118">Вы хотите изменить время, задержку, длительность или смещение кадров в группе анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="47c46-119">Редактирование Безье и изменение опорных кадров в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="47c46-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="47c46-120">Инспектор анимации поддерживает анимацию CSS, переходы CSS и веб-анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="47c46-121">анимации в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="47c46-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="47c46-122">Что такое группа анимации?</span><span class="sxs-lookup"><span data-stu-id="47c46-122">What is an Animation Group?</span></span>  

<span data-ttu-id="47c46-123">Группа анимации — это группа анимаций, которые могут быть связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="47c46-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="47c46-124">В настоящее время в веб-браузере отсутствует фактическая Концепция групповых анимаций, поэтому разработчики движений и разработчиков должны создавать и обрабатывать отдельные анимации, чтобы анимация отображалась как один и тот же визуальный эффект.</span><span class="sxs-lookup"><span data-stu-id="47c46-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="47c46-125">Инспектор анимации прогнозирует, какие анимации связаны с учетом времени начала, (за исключением задержек и т. д.).</span><span class="sxs-lookup"><span data-stu-id="47c46-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="47c46-126">Инспектор анимации также группирует анимацию рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="47c46-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="47c46-127">Другими словами, набор анимаций, которые вызываются в одном блоке сценария, группируются вместе.</span><span class="sxs-lookup"><span data-stu-id="47c46-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="47c46-128">Если анимация является асинхронной, она помещается в отдельную группу.</span><span class="sxs-lookup"><span data-stu-id="47c46-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="47c46-129">Начало работы</span><span class="sxs-lookup"><span data-stu-id="47c46-129">Get started</span></span>  

<span data-ttu-id="47c46-130">Открыть инспектор анимации можно двумя способами:</span><span class="sxs-lookup"><span data-stu-id="47c46-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="47c46-131">Открытие меню " **Настройка и управление DevTools** "</span><span class="sxs-lookup"><span data-stu-id="47c46-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="47c46-132">Перейдите к вложенному меню **другие инструменты** .</span><span class="sxs-lookup"><span data-stu-id="47c46-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="47c46-133">Выберите **анимации**:</span><span class="sxs-lookup"><span data-stu-id="47c46-133">Select **Animations**:</span></span>  
        
        > ##### <span data-ttu-id="47c46-134">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="47c46-134">Figure 2</span></span>  
        > <span data-ttu-id="47c46-135">Анимация с помощью главного меню</span><span class="sxs-lookup"><span data-stu-id="47c46-135">Animations via Main Menu</span></span>  
        > ![Анимация с помощью главного меню][ImageAnimationsViaMainMenu]  
        
*   <span data-ttu-id="47c46-137">Открытие **меню команд**</span><span class="sxs-lookup"><span data-stu-id="47c46-137">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="47c46-138">Введите `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="47c46-138">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="47c46-139">Инспектор анимации открывается в виде вкладки рядом с лотком консоли.</span><span class="sxs-lookup"><span data-stu-id="47c46-139">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="47c46-140">Поскольку инспектор анимаций является вкладкой ящика, вы можете использовать инспектор анимации на любой DevTools панели.</span><span class="sxs-lookup"><span data-stu-id="47c46-140">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

> ##### <span data-ttu-id="47c46-141">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="47c46-141">Figure 3</span></span>  
> <span data-ttu-id="47c46-142">Пустой инспектор анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-142">Empty Animation Inspector</span></span>  
> ![Пустой инспектор анимации][ImageEmptyAnimationInspector]  

<span data-ttu-id="47c46-144">Инспектор анимации сгруппирован в четыре основных раздела \ (или области).</span><span class="sxs-lookup"><span data-stu-id="47c46-144">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="47c46-145">Это руководство относится к каждой области, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="47c46-145">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="47c46-146">Панель</span><span class="sxs-lookup"><span data-stu-id="47c46-146">Pane</span></span> | <span data-ttu-id="47c46-147">Описание</span><span class="sxs-lookup"><span data-stu-id="47c46-147">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="47c46-148">1,1</span><span class="sxs-lookup"><span data-stu-id="47c46-148">1</span></span> | **<span data-ttu-id="47c46-149">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="47c46-149">Controls</span></span>** | <span data-ttu-id="47c46-150">Здесь вы можете очистить все текущие группы анимации или изменить скорость выбранной в данный момент группы анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-150">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="47c46-151">2</span><span class="sxs-lookup"><span data-stu-id="47c46-151">2</span></span> | **<span data-ttu-id="47c46-152">Обзор</span><span class="sxs-lookup"><span data-stu-id="47c46-152">Overview</span></span>** | <span data-ttu-id="47c46-153">Выберите группу анимации, чтобы проверить ее и изменить ее в области **сведений** .</span><span class="sxs-lookup"><span data-stu-id="47c46-153">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="47c46-154">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="47c46-154">3</span></span> | **<span data-ttu-id="47c46-155">Информация о сроках</span><span class="sxs-lookup"><span data-stu-id="47c46-155">Timeline</span></span>** | <span data-ttu-id="47c46-156">Задержите и начните анимацию отсюда или переходите к определенной точке анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-156">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="47c46-157">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="47c46-157">4</span></span> | **<span data-ttu-id="47c46-158">Сведения</span><span class="sxs-lookup"><span data-stu-id="47c46-158">Details</span></span>** | <span data-ttu-id="47c46-159">Проверка и изменение выбранной в данный момент группы эффектов анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-159">Inspect and modify the currently selected Animation Group.</span></span> |  

> ##### <span data-ttu-id="47c46-160">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="47c46-160">Figure 4</span></span>  
> <span data-ttu-id="47c46-161">Инспектор анимации с заметками</span><span class="sxs-lookup"><span data-stu-id="47c46-161">Annotated Animation Inspector</span></span>  
> ![Инспектор анимации с заметками][ImageAnnotatedAnimationInspector]  

<span data-ttu-id="47c46-163">Чтобы зафиксировать анимацию, просто выполните взаимодействие, которое запускает анимацию, когда открыт Инспектор анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-163">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="47c46-164">Если анимация запускается при загрузке страницы, перезагрузите страницу с помощью инспектора анимации, чтобы определить анимацию.</span><span class="sxs-lookup"><span data-stu-id="47c46-164">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="47c46-165">Проверка анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-165">Inspect animations</span></span>   

<span data-ttu-id="47c46-166">После захвата анимации есть несколько способов воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="47c46-166">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="47c46-167">Наведите указатель мыши на эскиз в области " **Обзор** ", чтобы просмотреть его в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="47c46-167">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="47c46-168">В области " **Обзор** " выберите группу анимации \ (чтобы она отображалась в области **сведений** ) и нажмите значок **воспроизведения** ![ ][ImageReplayButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="47c46-168">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** ![replay icon][ImageReplayButtonIcon] icon.</span></span>  <span data-ttu-id="47c46-169">Анимация воспроизводится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="47c46-169">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="47c46-170">**animation speed** ![ ][ImageAnimationSpeedButtonsIcon] Чтобы изменить скорость просмотра в выбранной группе эффектов анимации, щелкните значки скорость анимации анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-170">Click on the **animation speed** ![animation speed icons][ImageAnimationSpeedButtonsIcon] icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="47c46-171">Вы можете изменить текущее расположение с помощью красной вертикальной черты.</span><span class="sxs-lookup"><span data-stu-id="47c46-171">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="47c46-172">Щелкните и перетащите красную вертикальную полосу, чтобы проочистки анимации просмотра.</span><span class="sxs-lookup"><span data-stu-id="47c46-172">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  

### <span data-ttu-id="47c46-173">Просмотр подробных сведений о анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-173">View animation details</span></span>  

<span data-ttu-id="47c46-174">После захвата группы анимации щелкните ее в области " **Обзор** ", чтобы просмотреть подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="47c46-174">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="47c46-175">В области **сведений** каждая из анимаций назначается отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="47c46-175">In the **Details** pane each individual animation is assigned the a row.</span></span>  

> ##### <span data-ttu-id="47c46-176">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="47c46-176">Figure 5</span></span>  
> <span data-ttu-id="47c46-177">Сведения о группе эффектов анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-177">Animation Group details</span></span>  
> ![Сведения о группе эффектов анимации][ImageAnimationGroupDetails]  

<span data-ttu-id="47c46-179">Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="47c46-179">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="47c46-180">Щелкните анимацию, чтобы выделить ее на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="47c46-180">Click on the animation to select it in the **Elements** panel.</span></span>  

> ##### <span data-ttu-id="47c46-181">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="47c46-181">Figure 6</span></span>  
> <span data-ttu-id="47c46-182">Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра</span><span class="sxs-lookup"><span data-stu-id="47c46-182">Hover over the animation to highlight it in viewport</span></span>  
> ![Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра][ImageHoverOverAnimationHighlightViewport]  

<span data-ttu-id="47c46-184">Самым левым и темным разделом анимации является определение.</span><span class="sxs-lookup"><span data-stu-id="47c46-184">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="47c46-185">Справа, более размытые части представляют собой итерации.</span><span class="sxs-lookup"><span data-stu-id="47c46-185">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="47c46-186">Например, на [рисунке 7](#figure-7)разделы 2 и 3 представляют собой итерации раздела One.</span><span class="sxs-lookup"><span data-stu-id="47c46-186">For example, in [Figure 7](#figure-7), sections two and three represent iterations of section one.</span></span>  

> ##### <span data-ttu-id="47c46-187">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="47c46-187">Figure 7</span></span>  
> <span data-ttu-id="47c46-188">Схема итераций анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-188">Diagram of animation iterations</span></span>  
> ![Схема итераций анимации][ImageDiagramAnimationIterations]  

<span data-ttu-id="47c46-190">Если к двум элементам применена одинаковая анимация, инспектор анимации назначает элементам один и тот же цвет.</span><span class="sxs-lookup"><span data-stu-id="47c46-190">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="47c46-191">Цвет является произвольным и не имеет значимости.</span><span class="sxs-lookup"><span data-stu-id="47c46-191">The color is random and has no significance.</span></span>  <span data-ttu-id="47c46-192">Например, на [рисунке 8](#figure-8) используются два элемента с `div.cwccw.earlier` `div.cwccw.later` одинаковой анимацией \ ( `spinrightleft` \), как `div.ccwcw.earlier` и `div.ccwcw.later` элементы.</span><span class="sxs-lookup"><span data-stu-id="47c46-192">For example, in [Figure 8](#figure-8) the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

> ##### <span data-ttu-id="47c46-193">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="47c46-193">Figure 8</span></span>  
> <span data-ttu-id="47c46-194">Анимация с цветовым кодированием</span><span class="sxs-lookup"><span data-stu-id="47c46-194">Color-coded animations</span></span>  
> ![Анимация с цветовым кодированием][ImageColorCodedAnimations]  

## <span data-ttu-id="47c46-196">Изменение анимации</span><span class="sxs-lookup"><span data-stu-id="47c46-196">Modify animations</span></span>   

<span data-ttu-id="47c46-197">Вы можете изменить анимацию с помощью инспектора анимации тремя способами:</span><span class="sxs-lookup"><span data-stu-id="47c46-197">There are three ways you are able to modify an animation with the Animation Inspector:</span></span>  

*   <span data-ttu-id="47c46-198">Длительность анимации.</span><span class="sxs-lookup"><span data-stu-id="47c46-198">Animation duration.</span></span>  
*   <span data-ttu-id="47c46-199">Временные интервалы для ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="47c46-199">Keyframe timings.</span></span>  
*   <span data-ttu-id="47c46-200">Время начала задержки.</span><span class="sxs-lookup"><span data-stu-id="47c46-200">Start time delay.</span></span>  

<span data-ttu-id="47c46-201">В этом разделе показано, что [на рисунке 9](#figure-9) представлена исходная анимация.</span><span class="sxs-lookup"><span data-stu-id="47c46-201">For this section suppose that [Figure 9](#figure-9) represents the original animation:</span></span>  

> ##### <span data-ttu-id="47c46-202">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="47c46-202">Figure 9</span></span>  
> <span data-ttu-id="47c46-203">Исходная анимация перед изменением</span><span class="sxs-lookup"><span data-stu-id="47c46-203">Original animation before modification</span></span>  
> ![Исходная анимация перед изменением][ImageOriginalAnimationBeforeModification]  

<span data-ttu-id="47c46-205">Чтобы изменить длительность анимации, щелкните и перетащите первый или последний круг.</span><span class="sxs-lookup"><span data-stu-id="47c46-205">To change the duration of an animation, click and drag the first or last circle.</span></span>  

> ##### <span data-ttu-id="47c46-206">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="47c46-206">Figure 10</span></span>  
> <span data-ttu-id="47c46-207">Измененная длительность</span><span class="sxs-lookup"><span data-stu-id="47c46-207">Modified duration</span></span>  
> ![Измененная длительность][ImageModifiedDuration]  

<span data-ttu-id="47c46-209">Если анимация определяет любые правила для ключевого кадра, они будут представлены как белые внутренние круги.</span><span class="sxs-lookup"><span data-stu-id="47c46-209">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="47c46-210">Щелкните и перетащите один из них, чтобы изменить временные показатели для ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="47c46-210">Click and drag one of these to change the timing of the keyframe.</span></span>  

> ##### <span data-ttu-id="47c46-211">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="47c46-211">Figure 11</span></span>  
> <span data-ttu-id="47c46-212">Измененный ключевой кадр</span><span class="sxs-lookup"><span data-stu-id="47c46-212">Modified keyframe</span></span>  
> ![Измененный ключевой кадр][ImageModifiedKeyframe]  

<span data-ttu-id="47c46-214">Чтобы добавить задержку для анимации, щелкните и перетащите ее в любое место за исключением кругов.</span><span class="sxs-lookup"><span data-stu-id="47c46-214">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

> ##### <span data-ttu-id="47c46-215">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="47c46-215">Figure 12</span></span>  
> <span data-ttu-id="47c46-216">Измененная задержка</span><span class="sxs-lookup"><span data-stu-id="47c46-216">Modified delay</span></span>  
> ![Измененная задержка][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Рисунок 1: инспектор анимации"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Рисунок 2: анимация с помощью главного меню"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Рисунок 3: пустой инспектор анимации"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Рисунок 4: инспектор анимации с примечаниями"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Рисунок 5: сведения о группе эффектов анимации"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Рисунок 6: наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра"  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Рисунок 7: схема итераций анимации"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Рисунок 8: анимация с цветовым кодированием"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Рисунок 9: исходная анимация перед изменением"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Рисунок 10: изменена длительность"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Рисунок 11: изменен ключевой кадр"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Рисунок 12: измененная задержка"  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="47c46-230">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="47c46-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="47c46-231">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="47c46-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="47c46-233">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="47c46-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

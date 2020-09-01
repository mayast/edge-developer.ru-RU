---
title: Проверка эффектов анимации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a6970d76f4ff70031ef4cc8c6de119a41d1a5b80
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983417"
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





# <span data-ttu-id="03d7f-103">Проверка эффектов анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-103">Inspect animations</span></span>   



<span data-ttu-id="03d7f-104">Просмотрите и измените анимацию с помощью инспектора анимации Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="03d7f-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="03d7f-106">Инспектор анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-106">animation inspector</span></span>  
:::image-end:::  

### <span data-ttu-id="03d7f-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="03d7f-107">Summary</span></span>  

*   <span data-ttu-id="03d7f-108">Запишите анимацию, открыв инспектор анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-108">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="03d7f-109">Инспектор анимации автоматически определяет и сортирует анимации в группах.</span><span class="sxs-lookup"><span data-stu-id="03d7f-109">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="03d7f-110">Изучите анимацию, заменив каждую из них, воспроизводить каждую из них или просматривая исходный код.</span><span class="sxs-lookup"><span data-stu-id="03d7f-110">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="03d7f-111">Изменяйте анимацию, изменяя время, задержку, продолжительность или смещение опорных кадров.</span><span class="sxs-lookup"><span data-stu-id="03d7f-111">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="03d7f-112">Обзор</span><span class="sxs-lookup"><span data-stu-id="03d7f-112">Overview</span></span>   

<span data-ttu-id="03d7f-113">Инспектор анимации Microsoft Edge DevTools имеет два основных назначения.</span><span class="sxs-lookup"><span data-stu-id="03d7f-113">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="03d7f-114">Проверка анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-114">Inspecting animations.</span></span>  <span data-ttu-id="03d7f-115">Вы хотите замедлить, воспроизвести или проверить исходный код для группы анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-115">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="03d7f-116">Изменение анимаций.</span><span class="sxs-lookup"><span data-stu-id="03d7f-116">Modifying animations.</span></span>  <span data-ttu-id="03d7f-117">Вы хотите изменить время, задержку, длительность или смещение кадров в группе анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-117">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="03d7f-118">Редактирование Безье и изменение опорных кадров в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="03d7f-118">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="03d7f-119">Инспектор анимации поддерживает анимацию CSS, переходы CSS и веб-анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-119">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="03d7f-120">анимации в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="03d7f-120">animations are currently not supported.</span></span>  

### <span data-ttu-id="03d7f-121">Что такое группа анимации?</span><span class="sxs-lookup"><span data-stu-id="03d7f-121">What is an Animation Group?</span></span>  

<span data-ttu-id="03d7f-122">Группа анимации — это группа анимаций, которые могут быть связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="03d7f-122">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="03d7f-123">В настоящее время в веб-браузере отсутствует фактическая Концепция групповых анимаций, поэтому разработчики движений и разработчиков должны создавать и обрабатывать отдельные анимации, чтобы анимация отображалась как один и тот же визуальный эффект.</span><span class="sxs-lookup"><span data-stu-id="03d7f-123">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="03d7f-124">Инспектор анимации прогнозирует, какие анимации связаны с учетом времени начала, (за исключением задержек и т. д.).</span><span class="sxs-lookup"><span data-stu-id="03d7f-124">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="03d7f-125">Инспектор анимации также группирует анимацию рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="03d7f-125">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="03d7f-126">Другими словами, набор анимаций, которые вызываются в одном блоке сценария, группируются вместе.</span><span class="sxs-lookup"><span data-stu-id="03d7f-126">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="03d7f-127">Если анимация является асинхронной, она помещается в отдельную группу.</span><span class="sxs-lookup"><span data-stu-id="03d7f-127">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="03d7f-128">Get started</span><span class="sxs-lookup"><span data-stu-id="03d7f-128">Get started</span></span>  

<span data-ttu-id="03d7f-129">Открыть инспектор анимации можно двумя способами:</span><span class="sxs-lookup"><span data-stu-id="03d7f-129">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="03d7f-130">Открытие меню " **Настройка и управление DevTools** "</span><span class="sxs-lookup"><span data-stu-id="03d7f-130">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="03d7f-131">Перейдите к вложенному меню **другие инструменты** .</span><span class="sxs-lookup"><span data-stu-id="03d7f-131">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="03d7f-132">Выберите **анимации**:</span><span class="sxs-lookup"><span data-stu-id="03d7f-132">Select **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Анимация с помощью главного меню" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="03d7f-134">**Анимация** с помощью главного меню</span><span class="sxs-lookup"><span data-stu-id="03d7f-134">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="03d7f-135">Открытие **меню команд**</span><span class="sxs-lookup"><span data-stu-id="03d7f-135">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="03d7f-136">Введите `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="03d7f-136">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="03d7f-137">Инспектор анимации открывается в виде вкладки рядом с лотком консоли.</span><span class="sxs-lookup"><span data-stu-id="03d7f-137">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="03d7f-138">Поскольку инспектор анимаций является вкладкой ящика, вы можете использовать инспектор анимации на любой DevTools панели.</span><span class="sxs-lookup"><span data-stu-id="03d7f-138">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Пустой инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="03d7f-140">Пустой инспектор анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-140">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-141">Инспектор анимации сгруппирован в четыре основных раздела \ (или области).</span><span class="sxs-lookup"><span data-stu-id="03d7f-141">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="03d7f-142">Это руководство относится к каждой области, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="03d7f-142">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="03d7f-143">Панель</span><span class="sxs-lookup"><span data-stu-id="03d7f-143">Pane</span></span> | <span data-ttu-id="03d7f-144">Описание</span><span class="sxs-lookup"><span data-stu-id="03d7f-144">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="03d7f-145">1,1</span><span class="sxs-lookup"><span data-stu-id="03d7f-145">1</span></span> | **<span data-ttu-id="03d7f-146">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="03d7f-146">Controls</span></span>** | <span data-ttu-id="03d7f-147">Здесь вы можете очистить все текущие группы анимации или изменить скорость выбранной в данный момент группы анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-147">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="03d7f-148">2</span><span class="sxs-lookup"><span data-stu-id="03d7f-148">2</span></span> | **<span data-ttu-id="03d7f-149">Обзор</span><span class="sxs-lookup"><span data-stu-id="03d7f-149">Overview</span></span>** | <span data-ttu-id="03d7f-150">Выберите группу анимации, чтобы проверить ее и изменить ее в области **сведений** .</span><span class="sxs-lookup"><span data-stu-id="03d7f-150">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="03d7f-151">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="03d7f-151">3</span></span> | **<span data-ttu-id="03d7f-152">Информация о сроках</span><span class="sxs-lookup"><span data-stu-id="03d7f-152">Timeline</span></span>** | <span data-ttu-id="03d7f-153">Задержите и начните анимацию отсюда или переходите к определенной точке анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-153">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="03d7f-154">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="03d7f-154">4</span></span> | **<span data-ttu-id="03d7f-155">Сведения</span><span class="sxs-lookup"><span data-stu-id="03d7f-155">Details</span></span>** | <span data-ttu-id="03d7f-156">Проверка и изменение выбранной в данный момент группы эффектов анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-156">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Инспектор анимации с заметками" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="03d7f-158">Инспектор анимации с заметками</span><span class="sxs-lookup"><span data-stu-id="03d7f-158">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-159">Чтобы зафиксировать анимацию, просто выполните взаимодействие, которое запускает анимацию, когда открыт Инспектор анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-159">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="03d7f-160">Если анимация запускается при загрузке страницы, перезагрузите страницу с помощью инспектора анимации, чтобы определить анимацию.</span><span class="sxs-lookup"><span data-stu-id="03d7f-160">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="03d7f-161">Проверка эффектов анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-161">Inspect animations</span></span>   

<span data-ttu-id="03d7f-162">После захвата анимации есть несколько способов воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="03d7f-162">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="03d7f-163">Наведите указатель мыши на эскиз в области " **Обзор** ", чтобы просмотреть его в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="03d7f-163">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="03d7f-164">В области " **Обзор** " выберите группу анимации \ (чтобы она отображалась в области **сведений** ) и нажмите значок " **воспроизвести** " ( ![ значок воспроизведения ][ImageReplayButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="03d7f-164">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** \(![replay icon][ImageReplayButtonIcon]\) icon.</span></span>  <span data-ttu-id="03d7f-165">Анимация воспроизводится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="03d7f-165">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="03d7f-166">Щелкните значок **скорость анимации** \ ( ![ значки скорости анимации ][ImageAnimationSpeedButtonsIcon] \), чтобы изменить скорость просмотра выбранной группы анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-166">Click on the **animation speed** \(![animation speed icons][ImageAnimationSpeedButtonsIcon]\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="03d7f-167">Вы можете изменить текущее расположение с помощью красной вертикальной черты.</span><span class="sxs-lookup"><span data-stu-id="03d7f-167">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="03d7f-168">Щелкните и перетащите красную вертикальную полосу, чтобы проочистки анимации просмотра.</span><span class="sxs-lookup"><span data-stu-id="03d7f-168">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <span data-ttu-id="03d7f-169">Просмотр подробных сведений о анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-169">View animation details</span></span>  

<span data-ttu-id="03d7f-170">После захвата группы анимации щелкните ее в области " **Обзор** ", чтобы просмотреть подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="03d7f-170">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="03d7f-171">В области **сведений** каждая из анимаций назначается отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="03d7f-171">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Сведения о группе эффектов анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="03d7f-173">Сведения о группе эффектов анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-173">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-174">Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="03d7f-174">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="03d7f-175">Щелкните анимацию, чтобы выделить ее на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="03d7f-175">Click on the animation to select it in the **Elements** panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="03d7f-177">Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра</span><span class="sxs-lookup"><span data-stu-id="03d7f-177">Hover over the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-178">Самым левым и темным разделом анимации является определение.</span><span class="sxs-lookup"><span data-stu-id="03d7f-178">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="03d7f-179">Справа, более размытые части представляют собой итерации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-179">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="03d7f-180">Например, на приведенном ниже рисунке две и три части представляют собой итерации раздела One.</span><span class="sxs-lookup"><span data-stu-id="03d7f-180">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Схема итераций анимации" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="03d7f-182">Схема итераций анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-182">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-183">Если к двум элементам применена одинаковая анимация, инспектор анимации назначает элементам один и тот же цвет.</span><span class="sxs-lookup"><span data-stu-id="03d7f-183">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="03d7f-184">Цвет является произвольным и не имеет значимости.</span><span class="sxs-lookup"><span data-stu-id="03d7f-184">The color is random and has no significance.</span></span>  <span data-ttu-id="03d7f-185">Например, на приведенном ниже рисунке показаны два элемента `div.cwccw.earlier` и `div.cwccw.later` применена одинаковая анимация \ ( `spinrightleft` \), как `div.ccwcw.earlier` и `div.ccwcw.later` элементы.</span><span class="sxs-lookup"><span data-stu-id="03d7f-185">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Анимация с цветовым кодированием" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="03d7f-187">Анимация с цветовым кодированием</span><span class="sxs-lookup"><span data-stu-id="03d7f-187">Color-coded animations</span></span>  
:::image-end:::  

## <span data-ttu-id="03d7f-188">Изменение анимации</span><span class="sxs-lookup"><span data-stu-id="03d7f-188">Modify animations</span></span>   

<span data-ttu-id="03d7f-189">Вы можете изменить анимацию с помощью инспектора анимации тремя способами.</span><span class="sxs-lookup"><span data-stu-id="03d7f-189">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="03d7f-190">Длительность анимации.</span><span class="sxs-lookup"><span data-stu-id="03d7f-190">Animation duration.</span></span>  
*   <span data-ttu-id="03d7f-191">Временные интервалы для ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="03d7f-191">Keyframe timings.</span></span>  
*   <span data-ttu-id="03d7f-192">Время начала задержки.</span><span class="sxs-lookup"><span data-stu-id="03d7f-192">Start time delay.</span></span>  
    
<span data-ttu-id="03d7f-193">На приведенном ниже рисунке представлена исходная анимация.</span><span class="sxs-lookup"><span data-stu-id="03d7f-193">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Исходная анимация перед изменением" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="03d7f-195">Исходная анимация перед изменением</span><span class="sxs-lookup"><span data-stu-id="03d7f-195">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-196">Чтобы изменить длительность анимации, щелкните и перетащите первый или последний круг.</span><span class="sxs-lookup"><span data-stu-id="03d7f-196">To change the duration of an animation, click and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Измененная длительность" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="03d7f-198">Измененная длительность</span><span class="sxs-lookup"><span data-stu-id="03d7f-198">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-199">Если анимация определяет любые правила для ключевого кадра, они будут представлены как белые внутренние круги.</span><span class="sxs-lookup"><span data-stu-id="03d7f-199">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="03d7f-200">Щелкните и перетащите один из них, чтобы изменить временные показатели для ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="03d7f-200">Click and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Измененный ключевой кадр" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="03d7f-202">Измененный ключевой кадр</span><span class="sxs-lookup"><span data-stu-id="03d7f-202">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="03d7f-203">Чтобы добавить задержку для анимации, щелкните и перетащите ее в любое место за исключением кругов.</span><span class="sxs-lookup"><span data-stu-id="03d7f-203">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Измененная задержка" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="03d7f-205">Измененная задержка</span><span class="sxs-lookup"><span data-stu-id="03d7f-205">Modified delay</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="03d7f-206">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03d7f-206">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="03d7f-207">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="03d7f-207">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="03d7f-209">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03d7f-209">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

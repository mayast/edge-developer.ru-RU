---
title: Справка по специальным возможностям
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 7417388023612b6e1ca651deba28e099e3c8e3d8
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581575"
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





# <span data-ttu-id="653fd-103">Справка по специальным возможностям</span><span class="sxs-lookup"><span data-stu-id="653fd-103">Accessibility Reference</span></span>   



<span data-ttu-id="653fd-104">Эта страница является исчерпывающей ссылкой на специальные возможности в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="653fd-104">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="653fd-105">Оно предназначено для веб-разработчиков, которые:</span><span class="sxs-lookup"><span data-stu-id="653fd-105">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="653fd-106">Разработайте основные принципы DevTools, например, как открыть ее.</span><span class="sxs-lookup"><span data-stu-id="653fd-106">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="653fd-107">Знакомы с [принципами специальных возможностей и][MDNAccessibility]рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="653fd-107">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  

<span data-ttu-id="653fd-108">Цель этой ссылки — помочь вам найти все средства, доступные в DevTools, которые помогут вам изучить специальные возможности на странице.</span><span class="sxs-lookup"><span data-stu-id="653fd-108">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="653fd-109">Если вы ищете справку по переходу на DevTools с помощью специальных возможностей, таких как средство чтения с экрана, вы узнаете о том, что нужно сделать для навигации по [Microsoft Edge DevTools с технологией специальных возможностей][DevtoolsAccessibilityNavigation] .</span><span class="sxs-lookup"><span data-stu-id="653fd-109">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="653fd-110">Общие сведения о специальных возможностях в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="653fd-110">Overview of accessibility features in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="653fd-111">В этом разделе объясняется, как DevTools в общий набор средств для специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="653fd-111">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="653fd-112">Если вы решите, что страница доступна, вам нужно будет 2 общих вопросов.</span><span class="sxs-lookup"><span data-stu-id="653fd-112">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="653fd-113">Вы можете перемещаться по странице с помощью клавиатуры или [средства чтения с экрана][MDNScreenReader]?</span><span class="sxs-lookup"><span data-stu-id="653fd-113">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="653fd-114">Правильно ли помечены элементы страницы для средств чтения с экрана?</span><span class="sxs-lookup"><span data-stu-id="653fd-114">Are the elements of the page properly marked up for screen readers?</span></span>  

<span data-ttu-id="653fd-115">Как правило, DevTools поможет устранить ошибки, связанные с вопросами #2, так как эти ошибки легко выявить автоматически.</span><span class="sxs-lookup"><span data-stu-id="653fd-115">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="653fd-116">Вопрос #1 так же важен, но, к сожалению, DevTools не поможет вам.</span><span class="sxs-lookup"><span data-stu-id="653fd-116">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="653fd-117">Единственный способ найти ошибки, связанные с вопросом #1, — попытаться использовать страницу с помощью клавиатуры или средства чтения с экрана самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="653fd-117">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="653fd-118">Аудит специальных возможностей страницы</span><span class="sxs-lookup"><span data-stu-id="653fd-118">Audit the accessibility of a page</span></span>   

> [!NOTE]
> <span data-ttu-id="653fd-119">Панель **Аудит** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="653fd-119">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="653fd-120">Корпорация Майкрософт не несет ответственности за контент этих сайтов и любые данные, которые могут быть собраны, и не может контролировать их.</span><span class="sxs-lookup"><span data-stu-id="653fd-120">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="653fd-121">Как правило, с помощью панели аудит вы можете определить, есть ли в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="653fd-121">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="653fd-122">Страница правильно помечена для средств чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="653fd-122">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="653fd-123">Элементы текста на странице имеют достаточные коэффициенты контрастности.</span><span class="sxs-lookup"><span data-stu-id="653fd-123">The text elements on a page have sufficient contrast ratios.</span></span> <span data-ttu-id="653fd-124">Просмотрите также [коэффициент контрастности текстового элемента в средстве выбора цвета](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="653fd-124">See also [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="653fd-125">Чтобы выполнить аудит страницы, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="653fd-125">To audit a page:</span></span>  

1.  <span data-ttu-id="653fd-126">Перейдите к URL-адресу, на который вы хотите подвестись.</span><span class="sxs-lookup"><span data-stu-id="653fd-126">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="653fd-127">В DevTools откройте вкладку **аудитория** .  DevTools показывает различные параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="653fd-127">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    > ##### <span data-ttu-id="653fd-128">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="653fd-128">Figure 1</span></span>  
    > <span data-ttu-id="653fd-129">Настройка аудита</span><span class="sxs-lookup"><span data-stu-id="653fd-129">Configuring audits</span></span>  
    > ![Настройка аудита][ImageConfiguringAudits]  
    
    > [!NOTE]
    > <span data-ttu-id="653fd-131">Снимки экрана в этом разделе собраны в версии 79 Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="653fd-131">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="653fd-132">Вы можете проверить, на какой версии вы работаете `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="653fd-132">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="653fd-133">В более ранних версиях Microsoft Edge пользовательский интерфейс панели **аудита** выглядит иначе, но общий рабочий процесс одинаков.</span><span class="sxs-lookup"><span data-stu-id="653fd-133">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="653fd-134">Для **устройства**выберите **мобильные** устройства, если вы хотите имитировать мобильное устройство.</span><span class="sxs-lookup"><span data-stu-id="653fd-134">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="653fd-135">Этот параметр позволяет изменить строку вашего агента пользователя и изменить размер окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="653fd-135">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="653fd-136">Если Мобильная версия страницы отображается не так, как для классической версии, этот параметр может существенно повлиять на результаты аудита.</span><span class="sxs-lookup"><span data-stu-id="653fd-136">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="653fd-137">Убедитесь, что в разделе " **Аудит** " включен параметр " **Специальные возможности** ".</span><span class="sxs-lookup"><span data-stu-id="653fd-137">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="653fd-138">Отключите другие категории, если вы хотите исключить их из отчета.</span><span class="sxs-lookup"><span data-stu-id="653fd-138">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="653fd-139">Если вы хотите найти другие способы улучшить качество страницы, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="653fd-139">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="653fd-140">Раздел **регулирования** позволяет регулировать сеть и ЦП, что бывает полезно при анализе производительности нагрузки.</span><span class="sxs-lookup"><span data-stu-id="653fd-140">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="653fd-141">Этот параметр должен быть неважен для оценки доступности, поэтому вы можете использовать любой из них.</span><span class="sxs-lookup"><span data-stu-id="653fd-141">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="653fd-142">Флажок **clear Storage (очистить хранилище** ) позволяет очистить все хранилище перед загрузкой страницы или сохранением хранилища между загрузкой страниц.</span><span class="sxs-lookup"><span data-stu-id="653fd-142">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="653fd-143">Этот параметр также может быть неважен для оценки доступности, поэтому вы можете использовать любой из них.</span><span class="sxs-lookup"><span data-stu-id="653fd-143">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="653fd-144">Нажмите кнопку **запустить аудиты**.</span><span class="sxs-lookup"><span data-stu-id="653fd-144">Click **Run Audits**.</span></span> <span data-ttu-id="653fd-145">После 10 – 30 секунд DevTools предоставляет отчет.</span><span class="sxs-lookup"><span data-stu-id="653fd-145">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="653fd-146">В отчете приводятся различные советы по улучшению доступности страницы.</span><span class="sxs-lookup"><span data-stu-id="653fd-146">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    > ##### <span data-ttu-id="653fd-147">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="653fd-147">Figure 2</span></span>  
    > <span data-ttu-id="653fd-148">Отчет</span><span class="sxs-lookup"><span data-stu-id="653fd-148">A report</span></span>  
    > ![Отчет][ImageReport]  
    
1.  <span data-ttu-id="653fd-150">Щелкните аудиторию, чтобы получить дополнительные сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="653fd-150">Click an audit to learn more about it.</span></span>  
    
    > ##### <span data-ttu-id="653fd-151">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="653fd-151">Figure 3</span></span>  
    > <span data-ttu-id="653fd-152">Дополнительные сведения об аудите</span><span class="sxs-lookup"><span data-stu-id="653fd-152">More information about an audit</span></span>  
    > ![Дополнительные сведения об аудите][ImageAttributes]  
    
1.  <span data-ttu-id="653fd-154">Щелкните ссылку **Дополнительные сведения** , чтобы просмотреть документацию по аудиту.</span><span class="sxs-lookup"><span data-stu-id="653fd-154">Click **Learn More** to view the documentation of that audit.</span></span>
    
    > ##### <span data-ttu-id="653fd-155">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="653fd-155">Figure 4</span></span>  
    > <span data-ttu-id="653fd-156">Просмотр документации по аудиту</span><span class="sxs-lookup"><span data-stu-id="653fd-156">Viewing the documentation of an audit</span></span>  
    > ![Просмотр документации по аудиту][ImageAuditDocumentation]  
    
### <span data-ttu-id="653fd-158">Дополнительные сведения: расширение aXe</span><span class="sxs-lookup"><span data-stu-id="653fd-158">See also: aXe extension</span></span>   

<span data-ttu-id="653fd-159">Вы можете использовать [расширение aXe][ChromeWebStoreAxe] , а не панель **аудита** .</span><span class="sxs-lookup"><span data-stu-id="653fd-159">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="653fd-160">Расширение aXe обычно предоставляет те же сведения, так как это базовый обработчик, который включает в себя панель аудита.</span><span class="sxs-lookup"><span data-stu-id="653fd-160">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="653fd-161">Расширение aXe имеет другой пользовательский интерфейс и описывает аудит слегка разными способами.</span><span class="sxs-lookup"><span data-stu-id="653fd-161">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="653fd-162">Одно из преимуществ, которое имеет расширение aXe на панели **аудитов** , состоит в том, что она позволяет проверять и вымечать узлы, в которых произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="653fd-162">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

> ##### <span data-ttu-id="653fd-163">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="653fd-163">Figure 5</span></span>  
> <span data-ttu-id="653fd-164">Расширение aXe</span><span class="sxs-lookup"><span data-stu-id="653fd-164">The aXe extension</span></span>  
> ![Расширение aXe][ImageAxeExtension]  

## <span data-ttu-id="653fd-166">Область "Специальные возможности"</span><span class="sxs-lookup"><span data-stu-id="653fd-166">The Accessibility pane</span></span>   

<span data-ttu-id="653fd-167">В области " **Специальные возможности** " можно просмотреть дерево специальных возможностей, атрибуты ARIA и вычисляемые свойства специальных возможностей узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="653fd-167">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="653fd-168">Чтобы открыть область " **Специальные возможности** ", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="653fd-168">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="653fd-169">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="653fd-169">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="653fd-170">В **дереве DOM**выберите элемент, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="653fd-170">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="653fd-171">Откройте вкладку **Специальные возможности** .  Эта вкладка может быть скрыта за кнопкой **Дополнительные** вкладки ![ ][ImageMoreTabsIcon] .</span><span class="sxs-lookup"><span data-stu-id="653fd-171">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** ![More Tabs][ImageMoreTabsIcon] button.</span></span>  

> ##### <span data-ttu-id="653fd-172">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="653fd-172">Figure 6</span></span>  
> <span data-ttu-id="653fd-173">Проверка `h1` элемента домашней страницы DevTools в области " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="653fd-173">Inspecting the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
> ![Проверка элемента H1 на домашней странице DevTools в области "Специальные возможности"][ImageA11yPane]  

### <span data-ttu-id="653fd-175">Просмотр положения элемента в дереве специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="653fd-175">View the position of an element in the accessibility tree</span></span>   

<span data-ttu-id="653fd-176">[Дерево специальных возможностей][MDNAccessibilityTree] — это подмножество дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="653fd-176">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="653fd-177">Она включает только элементы из дерева DOM, которые являются важными и полезны для отображения содержимого страницы в средстве чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="653fd-177">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="653fd-178">Проверьте расположение элемента в дереве специальных возможностей в [области "Специальные возможности](#the-accessibility-pane)".</span><span class="sxs-lookup"><span data-stu-id="653fd-178">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="653fd-179">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="653fd-179">Figure 7</span></span>  
> <span data-ttu-id="653fd-180">Раздел дерева специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="653fd-180">The Accessibility Tree section</span></span>  
> ![Раздел дерева специальных возможностей][ImageAllyTree]  

### <span data-ttu-id="653fd-182">Просмотр атрибутов ARIA элемента</span><span class="sxs-lookup"><span data-stu-id="653fd-182">View the ARIA attributes of an element</span></span>   

<span data-ttu-id="653fd-183">Атрибуты ARIA гарантируют, что средства чтения с экрана имеют всю необходимую информацию для правильного представления содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="653fd-183">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="653fd-184">Просмотрите атрибуты ARIA элемента в [области "Специальные возможности](#the-accessibility-pane)".</span><span class="sxs-lookup"><span data-stu-id="653fd-184">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="653fd-185">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="653fd-185">Figure 8</span></span>  
> <span data-ttu-id="653fd-186">Раздел атрибутов ARIA</span><span class="sxs-lookup"><span data-stu-id="653fd-186">The ARIA Attributes section</span></span>  
> ![Раздел атрибутов ARIA][ImageAriaAttributesSection]  

### <span data-ttu-id="653fd-188">Просмотр вычисляемых свойств специальных возможностей для элемента</span><span class="sxs-lookup"><span data-stu-id="653fd-188">View the computed accessibility properties of an element</span></span>   

> [!NOTE]
> <span data-ttu-id="653fd-189">Если вы ищете вычисляемые свойства CSS, ознакомьтесь с [Разсчитанной вкладкой][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="653fd-189">If you are looking for computed CSS properties, see the [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="653fd-190">Некоторые свойства специальных возможностей динамически рассчитываются браузером.</span><span class="sxs-lookup"><span data-stu-id="653fd-190">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="653fd-191">Эти свойства отображаются в разделе " **вычисляемые свойства** " области " **Специальные возможности** ".</span><span class="sxs-lookup"><span data-stu-id="653fd-191">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="653fd-192">Просмотр вычисляемых свойств специальных возможностей для элемента в [области специальных возможностей](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="653fd-192">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="653fd-193">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="653fd-193">Figure 9</span></span>  
> <span data-ttu-id="653fd-194">Раздел свойств "вычисляемый (специальные возможности)"</span><span class="sxs-lookup"><span data-stu-id="653fd-194">The Computed (Accessibility) Properties section</span></span>  
> ![Раздел свойств "вычисляемый (специальные возможности)"][ImageComputedA11yPropertiesSection]  

## <span data-ttu-id="653fd-196">Просмотр коэффициента контрастности текстового элемента в палитре цветов</span><span class="sxs-lookup"><span data-stu-id="653fd-196">View the contrast ratio of a text element in the Color Picker</span></span>   

<span data-ttu-id="653fd-197">Некоторые люди со слабым зрением не видят области как очень яркие или очень темные.</span><span class="sxs-lookup"><span data-stu-id="653fd-197">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="653fd-198">Все обычно выводятся примерно одинаковая яркость, что делает ее более четкими и контурами.</span><span class="sxs-lookup"><span data-stu-id="653fd-198">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  
<span data-ttu-id="653fd-199">Коэффициент контрастности измеряет разницу яркости между передним и фоном текста.</span><span class="sxs-lookup"><span data-stu-id="653fd-199">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="653fd-200">Если текст имеет низкую степень контрастности, пользователи с низким зрением могут в буквальном смысле работать с вашим сайтом в качестве пустого экрана.</span><span class="sxs-lookup"><span data-stu-id="653fd-200">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="653fd-201">С помощью средства выбора цвета вы можете убедиться, что текст соответствует рекомендуемым уровням контрастности:</span><span class="sxs-lookup"><span data-stu-id="653fd-201">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="653fd-202">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="653fd-202">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="653fd-203">В **дереве DOM**выделите текстовый элемент, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="653fd-203">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    > ##### <span data-ttu-id="653fd-204">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="653fd-204">Figure 10</span></span>  
    > <span data-ttu-id="653fd-205">Проверка абзаца в дереве DOM</span><span class="sxs-lookup"><span data-stu-id="653fd-205">Inspecting a paragraph in the DOM Tree</span></span>  
    > ![Проверка абзаца в дереве DOM][ImageInspectDomTree]  
    
1.  <span data-ttu-id="653fd-207">В области **стили** щелкните квадратик цвета рядом со `color` значением элемента.</span><span class="sxs-lookup"><span data-stu-id="653fd-207">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    > ##### <span data-ttu-id="653fd-208">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="653fd-208">Figure 11</span></span>  
    > <span data-ttu-id="653fd-209">`color`Свойство элемента</span><span class="sxs-lookup"><span data-stu-id="653fd-209">The `color` property of the element</span></span>  
    > ![Свойство Color элемента][ImageColorElement]  
    
1.  <span data-ttu-id="653fd-211">Проверьте раздел **коэффициент контрастности** в палитре цветов.</span><span class="sxs-lookup"><span data-stu-id="653fd-211">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="653fd-212">Один флажок означает, что элемент соответствует [минимальным рекомендациям][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="653fd-212">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="653fd-213">Два флажка означают, что они соответствуют [улучшенным рекомендациям][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="653fd-213">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>
    
    > ##### <span data-ttu-id="653fd-214">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="653fd-214">Figure 12</span></span>  
    > <span data-ttu-id="653fd-215">В разделе "степень контрастности" в окне выбора цвета показаны 2 метки и значение</span><span class="sxs-lookup"><span data-stu-id="653fd-215">The Contrast Ratio section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    > ![В разделе "степень контрастности" в окне выбора цвета показаны 2 метки и значение 13,97][ImageColorPickerContrastRatio]  
    
1.  <span data-ttu-id="653fd-217">Щелкните раздел **коэффициент контрастности** , чтобы просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="653fd-217">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="653fd-218">В визуальном элементе выбора в верхней части окна выбора цвета появится линия.</span><span class="sxs-lookup"><span data-stu-id="653fd-218">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="653fd-219">Если текущий цвет соответствует рекомендациям, то все элементы на одной и той же стороне линии также соответствуют рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="653fd-219">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="653fd-220">Если текущий цвет не соответствует рекомендациям, то на одном и том же стороне не будут выводится соответствие рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="653fd-220">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    > ##### <span data-ttu-id="653fd-221">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="653fd-221">Figure 13</span></span>  
    > <span data-ttu-id="653fd-222">Линия коэффициента контрастности в средстве выбора визуальных элементов</span><span class="sxs-lookup"><span data-stu-id="653fd-222">The Contrast Ratio Line in the visual picker</span></span>  
    > ![Линия коэффициента контрастности в средстве выбора визуальных элементов][ImageContrastRatioLine]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  

[ImageConfiguringAudits]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-pane.msft.png "Рисунок 1: Настройка аудита"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result.msft.png "Рисунок 2."  
[ImageAttributes]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result-issues-expanded.msft.png "Рисунок 3: Дополнительные сведения об аудите"  
[ImageAuditDocumentation]: /microsoft-edge/devtools-guide-chromium/media/accessibility-web-dev-accessibility-audits-learn-more.msft.png "Рисунок 4: Просмотр документации по аудиту"  
[ImageAxeExtension]: /microsoft-edge/devtools-guide-chromium/media/accessibility-devtools-extension-axe-panel.msft.png "Рисунок 5: расширение aXe"  
[ImageA11yPane]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility.msft.png "Рисунок 6: Проверка элемента H1 на домашней странице DevTools в области "Специальные возможности""  
[ImageAllyTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-tree.msft.png "Рисунок 7: раздел дерева специальных возможностей"  
[ImageAriaAttributesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-aria-attributes.msft.png "Рисунок 8: раздел атрибуты ARIA"  
[ImageComputedA11yPropertiesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-computed-properties.msft.png "Рисунок 9: раздел свойства "вычисляемый (специальные возможности)""  
[ImageInspectDomTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-paragraph-highlight.msft.png "Рисунок 10: Проверка абзаца в дереве DOM"  
[ImageColorElement]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color.msft.png "Рисунок 11: свойство Color элемента"  
[ImageColorPickerContrastRatio]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png "Рисунок 12. в разделе "степень контрастности" в окне выбора цвета показаны 2 метки и значение 13,97"  
[ImageContrastRatioLine]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png "Рисунок 13: линия коэффициента контрастности в визуальном элементе выбора"  
<!-- links -->  

[DevtoolsAccessibilityNavigation]: navigation.md "Навигация в Microsoft Edge DevTools с помощью специальных возможностей"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Просмотр только CSS, которая фактически применяется к ссылке element-CSS"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe — тестирование специальных возможностей в Интернете-веб-магазин Chrome"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Дерево специальных возможностей (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Специальные возможности | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Средство чтения с экрана | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Контрастность (улучшенная) уровень AAA | PNG"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Контрастность (минимум) уровень AA | PNG"  

> [!NOTE]
> <span data-ttu-id="653fd-245">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="653fd-245">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="653fd-246">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="653fd-246">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="653fd-248">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="653fd-248">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

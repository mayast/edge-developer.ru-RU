---
title: Приступая к просмотру и изменению модели DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 4dee8b4e3ea927e72c0f98517f264b2c1d453013
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607449"
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





# <span data-ttu-id="cae26-103">Приступая к просмотру и изменению модели DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-103">Get Started With Viewing And Changing The DOM</span></span>   



<span data-ttu-id="cae26-104">Заполните эти интерактивные учебники, чтобы ознакомиться с основными принципами просмотра и изменения модели DOM на странице с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cae26-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="cae26-105">В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.</span><span class="sxs-lookup"><span data-stu-id="cae26-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="cae26-106">Ознакомьтесь с приложением [: HTML и модель DOM](#appendix-html-versus-the-dom) для объяснения.</span><span class="sxs-lookup"><span data-stu-id="cae26-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="cae26-107">Примеры открытых DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-107">Open DOM Examples</span></span>  

1.  <span data-ttu-id="cae26-108">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры DOM** , чтобы открыть ее на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="cae26-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="cae26-109">Примеры DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="cae26-110">Просмотр узлов DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-110">View DOM nodes</span></span>   

<span data-ttu-id="cae26-111">На панели "элементы" в дереве DOM можно выполнить все действия, связанные с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="cae26-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="cae26-112">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="cae26-112">Inspect a node</span></span>   

<span data-ttu-id="cae26-113">Если вы заинтересованы в определенном узле DOM, **Проверьте** , как быстро открыть DevTools и проанализировать этот узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="cae26-114">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-115">В разделе **Проверка узла**щелкните правой кнопкой мыши **Michelangelo** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="cae26-116">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="cae26-116">Figure 1</span></span>  
    > <span data-ttu-id="cae26-117">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="cae26-117">Inspecting a node</span></span>  
    > ![Проверка узла][ImageInspectingNode]  
    
    1.  <span data-ttu-id="cae26-119">Откроется панель " **элементы** " DevTools.</span><span class="sxs-lookup"><span data-stu-id="cae26-119">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="cae26-120">в **дереве DOM**выделено.</span><span class="sxs-lookup"><span data-stu-id="cae26-120">is highlighted in the **DOM Tree**.</span></span>  
        
        > ##### <span data-ttu-id="cae26-121">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="cae26-121">Figure 2</span></span>  
        > <span data-ttu-id="cae26-122">Выделение узла Michelangelo</span><span class="sxs-lookup"><span data-stu-id="cae26-122">Highlighting the Michelangelo node</span></span>  
        > ![Выделение узла Michelangelo][ImageHighlightingMichelangeloNode]  
        
        1.  <span data-ttu-id="cae26-124">Щелкните значок **проверки** ![ проверки ][ImageInspectIcon] в левом верхнем углу DevTools.</span><span class="sxs-lookup"><span data-stu-id="cae26-124">Click the **Inspect** ![Inspect][ImageInspectIcon] icon in the top-left corner of DevTools.</span></span>  
            
            > ##### <span data-ttu-id="cae26-125">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="cae26-125">Figure 3</span></span>  
            > <span data-ttu-id="cae26-126">Значок проверки</span><span class="sxs-lookup"><span data-stu-id="cae26-126">The Inspect icon</span></span>  
            > ![Значок проверки][ImageInspect]  
            
1.  <span data-ttu-id="cae26-128">В разделе **Проверка узла**щелкните текст в **Токио** .</span><span class="sxs-lookup"><span data-stu-id="cae26-128">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="cae26-129">Теперь `<li>Tokyo</li>` выделена в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-129">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="cae26-130">Проверка узла также является первым шагом в направлении просмотра и изменения стилей узла.</span><span class="sxs-lookup"><span data-stu-id="cae26-130">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="cae26-131">Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="cae26-131">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="cae26-132">Навигация по дереву DOM с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="cae26-132">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="cae26-133">После того как вы выбрали узел в дереве DOM, вы можете перемещаться по дереву DOM с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="cae26-133">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="cae26-134">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-134">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-135">В разделе **Навигация по дереву DOM с помощью клавиатуры**щелкните правой кнопкой мыши **Ringo** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-135">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="cae26-136">выбрано в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-136">is selected in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="cae26-137">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="cae26-137">Figure 4</span></span>  
    > <span data-ttu-id="cae26-138">Проверка узла Ringo</span><span class="sxs-lookup"><span data-stu-id="cae26-138">Inspecting the Ringo node</span></span>  
    > ![Проверка узла Ringo][ImageInspectingRingoNode]  
    
    1.  <span data-ttu-id="cae26-140">Нажимайте клавишу `Up` стрелка 2.</span><span class="sxs-lookup"><span data-stu-id="cae26-140">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="cae26-141">.</span><span class="sxs-lookup"><span data-stu-id="cae26-141">is selected.</span></span>  
        
        > ##### <span data-ttu-id="cae26-142">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="cae26-142">Figure 5</span></span>  
        > <span data-ttu-id="cae26-143">Проверка узла UL</span><span class="sxs-lookup"><span data-stu-id="cae26-143">Inspecting the ul node</span></span>  
        > ![Проверка узла UL][ImageInspectingUlNode]  
        
    1.  <span data-ttu-id="cae26-145">Нажмите клавишу `Left` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="cae26-145">Press the `Left` arrow key.</span></span>  <span data-ttu-id="cae26-146">`<ul>`Список сворачивается.</span><span class="sxs-lookup"><span data-stu-id="cae26-146">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="cae26-147">Снова нажмите клавишу `Left` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="cae26-147">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="cae26-148">Выбран родительский элемент `<ul>` узла.</span><span class="sxs-lookup"><span data-stu-id="cae26-148">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="cae26-149">В этом случае это `<div>` идентификатор `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="cae26-149">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="cae26-150">Нажимайте клавишу `Down` стрелка 2, чтобы повторно выбрать `<ul>` только что свернутый список.</span><span class="sxs-lookup"><span data-stu-id="cae26-150">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="cae26-151">Это должно выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cae26-151">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="cae26-152">Нажмите клавишу `Right` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="cae26-152">Press the `Right` arrow key.</span></span>  <span data-ttu-id="cae26-153">Список будет развернут.</span><span class="sxs-lookup"><span data-stu-id="cae26-153">The list expands.</span></span>  

### <span data-ttu-id="cae26-154">Прокрутка представления</span><span class="sxs-lookup"><span data-stu-id="cae26-154">Scroll into view</span></span>   

<span data-ttu-id="cae26-155">При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в данный момент не находится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="cae26-155">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="cae26-156">Например, предположим, что вы прокручивается в нижней части страницы, и вы заинтересованы в `<h1>` узле в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="cae26-156">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="cae26-157">**Прокрутка представления** позволяет быстро изменить расположение окна просмотра, чтобы вы могли видеть этот узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-157">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="cae26-158">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-158">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-159">В разделе **прокрутить представление**щелкните правой кнопкой мыши **Magritte** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-159">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="cae26-160">Прокрутите страницу "примеры DOM" до конца.</span><span class="sxs-lookup"><span data-stu-id="cae26-160">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="cae26-161">Этот `<li>Magritte</li>` узел по-прежнему должен быть выбран в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-161">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="cae26-162">В противном случае вернитесь на [страницу Просмотр](#scroll-into-view) и начните заново.</span><span class="sxs-lookup"><span data-stu-id="cae26-162">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="cae26-163">Щелкните правой кнопкой мыши `<li>Magritte</li>` узел и выберите **прокрутить до представления**.</span><span class="sxs-lookup"><span data-stu-id="cae26-163">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="cae26-164">Ваше окно просмотра будет прокручено, чтобы вы могли видеть узел **Magritte** .</span><span class="sxs-lookup"><span data-stu-id="cae26-164">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="cae26-165">Если вы не видите параметр **прокрутить в представлении** , вы можете просмотреть [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="cae26-165">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    > ##### <span data-ttu-id="cae26-166">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="cae26-166">Figure 6</span></span>  
    > <span data-ttu-id="cae26-167">Прокрутка представления</span><span class="sxs-lookup"><span data-stu-id="cae26-167">Scroll into view</span></span>  
    > ![Прокрутка представления][ImageScrollView]  

### <span data-ttu-id="cae26-169">Поиск узлов</span><span class="sxs-lookup"><span data-stu-id="cae26-169">Search for nodes</span></span>   

<span data-ttu-id="cae26-170">Вы можете выполнить поиск по дереву DOM по строке, селектору CSS или селектору XPath.</span><span class="sxs-lookup"><span data-stu-id="cae26-170">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="cae26-171">Сосредоточьте указатель мыши на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="cae26-171">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="cae26-172">Нажмите клавиши `Control` + `F` \ (Windows \) или `Command` + `F` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="cae26-172">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="cae26-173">Строка поиска откроется в нижней части дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-173">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="cae26-174">Введите `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="cae26-174">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="cae26-175">Последнее предложение выделено в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-175">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="cae26-176">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="cae26-176">Figure 7</span></span>  
    > <span data-ttu-id="cae26-177">Выделение запроса в строке поиска</span><span class="sxs-lookup"><span data-stu-id="cae26-177">Highlighting the query in the Search bar</span></span>  
    > ![Выделение запроса в строке поиска][ImageHighlightingQuerySearchBar]  
    
<span data-ttu-id="cae26-179">Как упоминалось выше, строка поиска также поддерживает селекторы CSS и XPath.</span><span class="sxs-lookup"><span data-stu-id="cae26-179">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="cae26-180">Редактирование модели DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-180">Edit the DOM</span></span>   

<span data-ttu-id="cae26-181">Вы можете изменить модель DOM на лету и посмотреть, как эти изменения влияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="cae26-181">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="cae26-182">Редактирование контента</span><span class="sxs-lookup"><span data-stu-id="cae26-182">Edit content</span></span>   

<span data-ttu-id="cae26-183">Чтобы изменить содержимое узла, дважды щелкните его содержимое в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-183">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="cae26-184">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-184">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-185">В разделе **изменить содержимое**щелкните правой кнопкой мыши **Мишель** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-185">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-186">В дереве DOM дважды щелкните `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="cae26-186">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="cae26-187">Другими словами, дважды щелкните текст между `<li>` and `</li>` .</span><span class="sxs-lookup"><span data-stu-id="cae26-187">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="cae26-188">Текст будет выделено, чтобы показать, что он выделен.</span><span class="sxs-lookup"><span data-stu-id="cae26-188">The text is highlighted to indicate that it is selected.</span></span>  
        
        > ##### <span data-ttu-id="cae26-189">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="cae26-189">Figure 8</span></span>  
        > <span data-ttu-id="cae26-190">Редактирование текста</span><span class="sxs-lookup"><span data-stu-id="cae26-190">Editing the text</span></span>  
        > ![Редактирование текста][ImageEditingText]  
        
    1.  <span data-ttu-id="cae26-192">Удалить `Michelle` , введите `Leela` и нажмите кнопку, `Enter` чтобы подтвердить изменение.</span><span class="sxs-lookup"><span data-stu-id="cae26-192">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="cae26-193">Текст в DOM изменится с **Мишель** на **Leela**.</span><span class="sxs-lookup"><span data-stu-id="cae26-193">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="cae26-194">Изменение атрибутов</span><span class="sxs-lookup"><span data-stu-id="cae26-194">Edit attributes</span></span>   

<span data-ttu-id="cae26-195">Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="cae26-195">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="cae26-196">Следуйте инструкциям, чтобы научиться добавлять атрибуты на узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-196">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="cae26-197">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-197">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-198">В разделе **изменить атрибуты**щелкните правой кнопкой мыши **Говард** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-198">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  

1.  <span data-ttu-id="cae26-199">Дважды щелкните `<li>` .</span><span class="sxs-lookup"><span data-stu-id="cae26-199">Double-click `<li>`.</span></span>  <span data-ttu-id="cae26-200">Текст будет выделено, чтобы показать, что выбран узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-200">The text is highlighted to indicate that the node is selected.</span></span>  
    
    > ##### <span data-ttu-id="cae26-201">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="cae26-201">Figure 9</span></span>  
    > <span data-ttu-id="cae26-202">Редактирование узла</span><span class="sxs-lookup"><span data-stu-id="cae26-202">Editing the node</span></span>  
    > ![Редактирование узла][ImageEditingNode]  
    
1.  <span data-ttu-id="cae26-204">Нажимайте клавишу `Right` со стрелкой, добавьте пробел, введите текст `style="background-color:gold"` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cae26-204">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="cae26-205">Цвет фона узла изменится на Золотой.</span><span class="sxs-lookup"><span data-stu-id="cae26-205">The background color of the node changes to gold.</span></span>  
    
    > ##### <span data-ttu-id="cae26-206">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="cae26-206">Figure 10</span></span>  
    > <span data-ttu-id="cae26-207">Добавление атрибута стиля на узел</span><span class="sxs-lookup"><span data-stu-id="cae26-207">Adding a style attribute to the node</span></span>  
    > ![Добавление атрибута стиля на узел][ImageAddingStyleAttributeNode]  
    
### <span data-ttu-id="cae26-209">Изменить тип узла</span><span class="sxs-lookup"><span data-stu-id="cae26-209">Edit node type</span></span>   

<span data-ttu-id="cae26-210">Чтобы изменить тип узла, дважды щелкните его, а затем введите новый тип.</span><span class="sxs-lookup"><span data-stu-id="cae26-210">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="cae26-211">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-212">В разделе **изменить тип узла**щелкните правой кнопкой мыши **Hank** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-212">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-213">Дважды щелкните `<li>` .</span><span class="sxs-lookup"><span data-stu-id="cae26-213">Double-click `<li>`.</span></span>  <span data-ttu-id="cae26-214">Текст `li` будет выделен.</span><span class="sxs-lookup"><span data-stu-id="cae26-214">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="cae26-215">Удалить `li` , введите `button` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cae26-215">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="cae26-216">`<li>`Узел изменится на `<button>` узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-216">The `<li>` node changes to a `<button>` node.</span></span>  
        
        > ##### <span data-ttu-id="cae26-217">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="cae26-217">Figure 11</span></span>  
        > <span data-ttu-id="cae26-218">Изменение типа узла на кнопку</span><span class="sxs-lookup"><span data-stu-id="cae26-218">Changing the node type to button</span></span>  
        > ![Изменение типа узла на кнопку][ImageChangingNodeButton]  
        
### <span data-ttu-id="cae26-220">Изменение порядка узлов DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-220">Reorder DOM nodes</span></span>   

<span data-ttu-id="cae26-221">Перетащите узлы, чтобы изменить их порядок.</span><span class="sxs-lookup"><span data-stu-id="cae26-221">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="cae26-222">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-222">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-223">В разделе **изменение порядка узлов DOM**щелкните **Elvis Presley** правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-223">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cae26-224">Это последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="cae26-224">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="cae26-225">В дереве DOM перетащите указатель `<li>Elvis Presley</li>` в верхнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="cae26-225">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        > ##### <span data-ttu-id="cae26-226">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="cae26-226">Figure 12</span></span>  
        > <span data-ttu-id="cae26-227">Перетаскивание узла в верхнюю часть списка</span><span class="sxs-lookup"><span data-stu-id="cae26-227">Dragging the node to the top of the list</span></span>  
        > ![Перетаскивание узла в верхнюю часть списка][ImageDraggingNodeTopList]  
        
### <span data-ttu-id="cae26-229">Принудительное состояние</span><span class="sxs-lookup"><span data-stu-id="cae26-229">Force state</span></span>   

<span data-ttu-id="cae26-230">Вы можете принудительно оставлять узлы в состоянии, в том числе,,, `:active` `:hover` `:focus` `:visited` и `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="cae26-230">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="cae26-231">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-231">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-232">В разделе **принудительное состояние**наведите указатель мыши на **Lord летит**.</span><span class="sxs-lookup"><span data-stu-id="cae26-232">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="cae26-233">Цвет фона становится оранжевым.</span><span class="sxs-lookup"><span data-stu-id="cae26-233">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="cae26-234">Щелкните **Lord летит** правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-234">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-235">Щелкните правой кнопкой мыши `<li class="demo--hover">The Lord of the Flies</li>` и выберите **принудительное состояние**  >  **: наведение**.</span><span class="sxs-lookup"><span data-stu-id="cae26-235">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="cae26-236">Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="cae26-236">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="cae26-237">Цвет фона остается оранжевым, несмотря на то что вы не наводите указатель мыши на узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-237">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="cae26-238">Скрытие узла</span><span class="sxs-lookup"><span data-stu-id="cae26-238">Hide a node</span></span>   

<span data-ttu-id="cae26-239">Нажмите `H` , чтобы скрыть узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-239">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="cae26-240">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-240">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-241">В разделе **скрыть узел**щелкните правой кнопкой мыши **звезду назначения** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-241">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-242">Нажмите клавишу `H` .</span><span class="sxs-lookup"><span data-stu-id="cae26-242">Press the `H` key.</span></span>  <span data-ttu-id="cae26-243">Узел скрыт.</span><span class="sxs-lookup"><span data-stu-id="cae26-243">The node is hidden.</span></span>  
        
        > ##### <span data-ttu-id="cae26-244">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="cae26-244">Figure 13</span></span>  
        > <span data-ttu-id="cae26-245">Как выглядит узел в дереве DOM после его скрытия</span><span class="sxs-lookup"><span data-stu-id="cae26-245">What the node looks like in the DOM Tree after it is hidden</span></span>  
        > ![Как выглядит узел в дереве DOM после его скрытия][ImageNodeDomTreeAfterHidden]  
        
    1.  <span data-ttu-id="cae26-247">Снова нажмите клавишу `H` .</span><span class="sxs-lookup"><span data-stu-id="cae26-247">Press the `H` key again.</span></span>  <span data-ttu-id="cae26-248">Узел снова появится.</span><span class="sxs-lookup"><span data-stu-id="cae26-248">The node is shown again.</span></span>  

### <span data-ttu-id="cae26-249">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="cae26-249">Delete a node</span></span>   

<span data-ttu-id="cae26-250">Нажмите `Delete` , чтобы удалить узел.</span><span class="sxs-lookup"><span data-stu-id="cae26-250">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="cae26-251">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-251">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-252">В разделе **Удаление узла**щелкните правой кнопкой мыши элемент **Foundation** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-252">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-253">Нажмите клавишу `Delete` .</span><span class="sxs-lookup"><span data-stu-id="cae26-253">Press the `Delete` key.</span></span>  <span data-ttu-id="cae26-254">Узел удален.</span><span class="sxs-lookup"><span data-stu-id="cae26-254">The node is deleted.</span></span>  
    1.  <span data-ttu-id="cae26-255">Нажмите клавиши `Control` + `Z` \ (Windows \) или `Command` + `Z` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="cae26-255">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="cae26-256">Последнее действие отменено, и узел появится снова.</span><span class="sxs-lookup"><span data-stu-id="cae26-256">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="cae26-257">Узлы Access на консоли</span><span class="sxs-lookup"><span data-stu-id="cae26-257">Access nodes in the Console</span></span>   

<span data-ttu-id="cae26-258">DevTools предоставляет несколько сочетаний клавиш для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждую из них.</span><span class="sxs-lookup"><span data-stu-id="cae26-258">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="cae26-259">Ссылка на узел, выбранный в настоящее время с помощью $0</span><span class="sxs-lookup"><span data-stu-id="cae26-259">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="cae26-260">Когда вы просматриваете узел, `== $0` текст рядом с узлом означает, что вы можете добавить ссылку на этот узел в консоль с переменной `$0` .</span><span class="sxs-lookup"><span data-stu-id="cae26-260">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="cae26-261">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-261">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-262">В разделе **ссылка на узел, выбранный в $0**, щелкните правой кнопкой мыши **в левой части экрана** , а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-262">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-263">Нажмите клавишу, `Escape` чтобы открыть консольный ящик.</span><span class="sxs-lookup"><span data-stu-id="cae26-263">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="cae26-264">Введите текст и нажмите клавишу ВВОД `$0` `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cae26-264">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="cae26-265">Результат выражения показывает, что выражение `$0` имеет значение `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="cae26-265">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        > ##### <span data-ttu-id="cae26-266">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="cae26-266">Figure 14</span></span>  
        > <span data-ttu-id="cae26-267">Результат первого `$0` выражения в консоли</span><span class="sxs-lookup"><span data-stu-id="cae26-267">The result of the first `$0` expression in the Console</span></span>  
        > ![Результат первого выражения $0 в консоли][ImageFirstConsole]  
        
    1.  <span data-ttu-id="cae26-269">Наведите указатель мыши на результат.</span><span class="sxs-lookup"><span data-stu-id="cae26-269">Hover over the result.</span></span>  <span data-ttu-id="cae26-270">Узел выделится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="cae26-270">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="cae26-271">Щелкните `<li>Dune</li>` дерево DOM, введите `$0` консоль еще раз, а затем нажмите `Enter` еще раз.</span><span class="sxs-lookup"><span data-stu-id="cae26-271">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="cae26-272">Теперь `$0` оценивается `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="cae26-272">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        > ##### <span data-ttu-id="cae26-273">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="cae26-273">Figure 15</span></span>  
        > <span data-ttu-id="cae26-274">Результат второго `$0` выражения на консоли — ![ результат второго выражения $0 в консоли.][ImageSecondConsole]</span><span class="sxs-lookup"><span data-stu-id="cae26-274">The result of the second `$0` expression in the Console ![The result of the second $0 expression in the Console][ImageSecondConsole]</span></span>  
        
### <span data-ttu-id="cae26-275">Сохранить как глобальную переменную</span><span class="sxs-lookup"><span data-stu-id="cae26-275">Store as global variable</span></span>   

<span data-ttu-id="cae26-276">Если необходимо повторно сослаться на узел, сохраните его как глобальную переменную.</span><span class="sxs-lookup"><span data-stu-id="cae26-276">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="cae26-277">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-277">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-278">В разделе **Сохранить как глобальную переменную**щелкните правой кнопкой мыши **в большом спящем режиме** и выберите **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-278">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-279">Щелкните правой кнопкой мыши `<li>The Big Sleep</li>` дерево DOM и выберите **Сохранить как глобальную переменную**.</span><span class="sxs-lookup"><span data-stu-id="cae26-279">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="cae26-280">Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="cae26-280">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="cae26-281">Введите текст `temp1` на консоли и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cae26-281">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="cae26-282">Результат выражения показывает, что переменная является узлом.</span><span class="sxs-lookup"><span data-stu-id="cae26-282">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        > ##### <span data-ttu-id="cae26-283">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="cae26-283">Figure 16</span></span>  
        > <span data-ttu-id="cae26-284">Результат выражения temp1</span><span class="sxs-lookup"><span data-stu-id="cae26-284">The result of the temp1 expression</span></span>  
        > ![Результат выражения temp1][ImageResultTemp1]  
        
### <span data-ttu-id="cae26-286">Скопировать путь к JS</span><span class="sxs-lookup"><span data-stu-id="cae26-286">Copy JS path</span></span>   

<span data-ttu-id="cae26-287">Скопируйте путь JavaScript на узел, если вам нужно сослаться на него в автоматическом тесте.</span><span class="sxs-lookup"><span data-stu-id="cae26-287">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="cae26-288">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-288">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-289">В разделе **скопировать путь к каталогу**щелкните правой кнопкой мыши **братьев Karamazov** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-289">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-290">Щелкните правой кнопкой мыши `<li>The Brothers Karamazov</li>` дерево DOM и выберите команду **Копировать**  >  **путь к каталогу**.</span><span class="sxs-lookup"><span data-stu-id="cae26-290">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="cae26-291">`document.querySelector()`Выражение, которое разрешается в узел, копируется в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="cae26-291">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="cae26-292">`Control` + `V` Чтобы вставить выражение на консоль, нажмите клавиши \ (Windows \) или `Command` + `V` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="cae26-292">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="cae26-293">Нажмите `Enter` , чтобы вычислить выражение.</span><span class="sxs-lookup"><span data-stu-id="cae26-293">Press `Enter` to evaluate the expression.</span></span>
        
        > ##### <span data-ttu-id="cae26-294">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="cae26-294">Figure 17</span></span>  
        > <span data-ttu-id="cae26-295">Результат выражения Copy JS Path</span><span class="sxs-lookup"><span data-stu-id="cae26-295">The result of the Copy JS Path expression</span></span>  
        > ![Результат выражения Copy JS Path][ImageResultCopyJSPath]  
        
## <span data-ttu-id="cae26-297">Прерывание изменений DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-297">Break on DOM changes</span></span>   

<span data-ttu-id="cae26-298">DevTools позволяет приостановить JavaScript на странице, когда JavaScript изменит модель DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-298">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="cae26-299">Прерывание изменений атрибутов</span><span class="sxs-lookup"><span data-stu-id="cae26-299">Break on attribute modifications</span></span>   

<span data-ttu-id="cae26-300">Используйте точки останова по изменению атрибутов, если требуется приостановить JavaScript, который приводит к изменению любого атрибута узла.</span><span class="sxs-lookup"><span data-stu-id="cae26-300">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="cae26-301">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-301">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-302">В разделе **прервать на странице "изменения атрибутов**" щелкните правой кнопкой мыши **Sauerkraut** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-302">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-303">В дереве DOM щелкните правой кнопкой мыши `<li id="target">Sauerkraut</li>` и выберите команду **прервать для**  >  **изменений атрибутов**.</span><span class="sxs-lookup"><span data-stu-id="cae26-303">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="cae26-304">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="cae26-304">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        > ##### <span data-ttu-id="cae26-305">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="cae26-305">Figure 18</span></span>  
        > <span data-ttu-id="cae26-306">Прерывание изменений атрибутов</span><span class="sxs-lookup"><span data-stu-id="cae26-306">Break on attribute modifications</span></span>  
        > ![Прерывание изменений атрибутов][ImageBreakAttributeModification]  
        
    1.  <span data-ttu-id="cae26-308">На следующем этапе вы будете получать инструкции по нажатию кнопки, которая приостанавливает код страницы.</span><span class="sxs-lookup"><span data-stu-id="cae26-308">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="cae26-309">После того как страница приостановлена, прокрутка страницы больше недоступна.</span><span class="sxs-lookup"><span data-stu-id="cae26-309">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="cae26-310">**Resume Script** ![ ][ImageResumeScriptIcon] Чтобы снова выполнить прокрутку страницы, необходимо выбрать команду возобновить сценарий возобновления.</span><span class="sxs-lookup"><span data-stu-id="cae26-310">You must click **Resume Script** ![Resume Script][ImageResumeScriptIcon] in order to make the page scrollable again.</span></span>
        
        > ##### <span data-ttu-id="cae26-311">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="cae26-311">Figure 19</span></span>  
        > <span data-ttu-id="cae26-312">Как возобновить выполнение сценария</span><span class="sxs-lookup"><span data-stu-id="cae26-312">Where to resume script running</span></span>  
        > ![Как возобновить выполнение сценария][ImageResumeScript]  
        
    1.  <span data-ttu-id="cae26-314">Нажмите кнопку " **настроить фон** ".</span><span class="sxs-lookup"><span data-stu-id="cae26-314">Click the **Set Background** button above.</span></span>  <span data-ttu-id="cae26-315">Таким образом, `style` для атрибута узла будет задано значение `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="cae26-315">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="cae26-316">DevTools приостанавливает страницу и выделяет код, который привел к изменению атрибута.</span><span class="sxs-lookup"><span data-stu-id="cae26-316">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="cae26-317">Нажмите кнопку **возобновить** сценарий ![ резюме ][ImageResumeScriptIcon] , как упоминалось ранее.</span><span class="sxs-lookup"><span data-stu-id="cae26-317">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon], as mentioned earlier.</span></span>  
    
### <span data-ttu-id="cae26-318">Прерывание при удалении узла</span><span class="sxs-lookup"><span data-stu-id="cae26-318">Break on node removal</span></span>   

<span data-ttu-id="cae26-319">Если вы хотите приостановить работу при удалении определенного узла, используйте точки останова удаления узла.</span><span class="sxs-lookup"><span data-stu-id="cae26-319">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="cae26-320">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-320">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-321">В разделе **прервать удаление узла**щелкните правой кнопкой мыши **Neuromancer** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-321">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-322">В дереве DOM щелкните правой кнопкой мыши `<li id="target">Neuromancer</li>` и выберите команду **прервать при**  >  **удалении узла**.</span><span class="sxs-lookup"><span data-stu-id="cae26-322">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="cae26-323">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="cae26-323">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="cae26-324">Нажмите кнопку " **Удалить** ".</span><span class="sxs-lookup"><span data-stu-id="cae26-324">Click the **Delete** button above.</span></span>  <span data-ttu-id="cae26-325">DevTools приостанавливает страницу и выделяет код, вызвавший удаление узла.</span><span class="sxs-lookup"><span data-stu-id="cae26-325">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="cae26-326">Нажмите кнопку **возобновить** сценарий ![ возобновления ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="cae26-326">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
### <span data-ttu-id="cae26-327">Прерывание при изменении поддерева</span><span class="sxs-lookup"><span data-stu-id="cae26-327">Break on subtree modifications</span></span>   

<span data-ttu-id="cae26-328">После того как вы добавите на узел точку останова изменения поддерева, DevTools приостанавливает страницу при добавлении или удалении любого потомка узла.</span><span class="sxs-lookup"><span data-stu-id="cae26-328">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="cae26-329">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="cae26-329">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="cae26-330">В разделе **прервать при изменении поддерева**щелкните правой кнопкой мыши значок **Fire** и выберите пункт **проверить**.</span><span class="sxs-lookup"><span data-stu-id="cae26-330">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="cae26-331">В дереве DOM щелкните правой кнопкой мыши расположенный `<ul id="target">` выше узел `<li>A Fire Upon the Deep</li>` и выберите команду **приостановить**  >  **изменение поддерева**.</span><span class="sxs-lookup"><span data-stu-id="cae26-331">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="cae26-332">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="cae26-332">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="cae26-333">Нажмите кнопку **Добавить ребенка**.</span><span class="sxs-lookup"><span data-stu-id="cae26-333">Click **Add Child**.</span></span>  <span data-ttu-id="cae26-334">Код приостанавливается, так как `<li>` узел был добавлен в список.</span><span class="sxs-lookup"><span data-stu-id="cae26-334">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="cae26-335">Нажмите кнопку **возобновить** сценарий ![ возобновления ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="cae26-335">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
## <span data-ttu-id="cae26-336">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cae26-336">Next steps</span></span>   

<span data-ttu-id="cae26-337">, Которая охватывает большую часть функций, связанных с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="cae26-337">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="cae26-338">Вы можете найти остальные элементы, щелкнув правой кнопкой мыши узлы в дереве DOM и экспериментируя с другими параметрами, которые не были рассмотрены в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="cae26-338">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="cae26-339">Вы также можете просмотреть [сочетания клавиш для панели элементов][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="cae26-339">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="cae26-340">Ознакомьтесь с [домашней страницей Microsoft Edge DevTools][MicrosoftEdgeDevTools] , чтобы найти все, что вы можете делать с DevTools.</span><span class="sxs-lookup"><span data-stu-id="cae26-340">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="cae26-341">Приложение: HTML и модель DOM</span><span class="sxs-lookup"><span data-stu-id="cae26-341">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="cae26-342">В этом разделе приводится описание различий между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-342">This section quickly explains the difference between HTML and the DOM.</span></span>  

<span data-ttu-id="cae26-343">При использовании веб-браузера для запроса страницы сервер возвращает HTML-код следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cae26-343">When you use a web browser to request a page, the server returns HTML like this:</span></span>  

```html
<!doctype html>
<html>
  <head>
    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <p>This is a hypertext document on the World Wide Web.</p>
    <script src="/script.js" async></script>
  </body>
</html>
```  

<span data-ttu-id="cae26-344">Браузер анализирует HTML-код и создает дерево объектов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="cae26-344">The browser parses the HTML and creates a tree of objects like this:</span></span>  

```dom
html
  head
    title
  body
    h1
    p
    script
```  

<span data-ttu-id="cae26-345">Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-345">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  <span data-ttu-id="cae26-346">Теперь он выглядит так же, как HTML, но предположим, что сценарий, указанный в нижней части HTML, выполняет этот код:</span><span class="sxs-lookup"><span data-stu-id="cae26-346">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs this code:</span></span>  

```javascript
const h1 = document.querySelector('h1');
h1.parentElement.removeChild(h1);
const p = document.createElement('p');
p.textContent = 'Wildcard!';
document.body.appendChild(p);
```  

<span data-ttu-id="cae26-347">Этот код удаляет `h1` узел и добавляет еще один `p` узел в модель DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-347">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="cae26-348">Полная модель DOM теперь выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cae26-348">The complete DOM now looks like this:</span></span>  

```dom
html
  head
    title
  body
    p
    script
    p
```  

<span data-ttu-id="cae26-349">HTML-код страницы теперь отличается от модели DOM.</span><span class="sxs-lookup"><span data-stu-id="cae26-349">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="cae26-350">Другими словами, HTML представляет начальное содержимое страницы, а модель DOM — текущее содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="cae26-350">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="cae26-351">Когда JavaScript добавляет, удаляет или редактирует узлы, модель DOM становится отличной от HTML.</span><span class="sxs-lookup"><span data-stu-id="cae26-351">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="cae26-352">Дополнительные сведения можно найти в разделе [Введение в модель DOM][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="cae26-352">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > ![Scroll into view][ImageScrollView]  
    -->  

## <span data-ttu-id="cae26-353">Приложение: отсутствующие параметры</span><span class="sxs-lookup"><span data-stu-id="cae26-353">Appendix: Missing options</span></span>   

<span data-ttu-id="cae26-354">Многие инструкции, описанные в этом руководстве, помогут вам щелкнуть правой кнопкой мыши узел в дереве DOM и выбрать нужный вариант в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="cae26-354">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="cae26-355">Если указанный параметр не отображается в контекстном меню, попробуйте щелкнуть правой кнопкой мыши за пределами текста узла.</span><span class="sxs-lookup"><span data-stu-id="cae26-355">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

> ##### <span data-ttu-id="cae26-356">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="cae26-356">Figure 20</span></span>  
> <span data-ttu-id="cae26-357">Выбор варианта, если вы не видите все параметры</span><span class="sxs-lookup"><span data-stu-id="cae26-357">Where to click if you are not seeing all the options</span></span>  
> ![Выбор варианта, если вы не видите все параметры][ImageNotSeeingAllOptions]  

<!-- image links -->  

[ImageInspectIcon]: /microsoft-edge/devtools-guide-chromium/media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-icon.msft.png  

[ImageInspectingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-inspect.msft.png "Рисунок 1: Проверка узла"  
[ImageHighlightingMichelangeloNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png "Рисунок 2: выделение узла Michelangelo"  
[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-select-element-page-inspect.msft.png "Рисунок 3: значок проверки"  
[ImageInspectingRingoNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png "Рисунок 4: Проверка узла Ringo"  
[ImageInspectingUlNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png "Рисунок 5: Проверка узла UL"  
[ImageScrollView]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png "Рисунок 6: прокрутка представления"  
[ImageHighlightingQuerySearchBar]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-search-nodes-highlight.msft.png "Рисунок 7: выделение запроса в строке поиска"  
[ImageEditingText]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-content.msft.png "Рисунок 8: Редактирование текста"  
[ImageEditingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-highlighted.msft.png "Рисунок 9: Редактирование узла"  
[ImageAddingStyleAttributeNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-inline-css.msft.png "Рисунок 10: Добавление атрибута стиля на узел"  
[ImageChangingNodeButton]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-node-type-button.msft.png "Рисунок 11. изменение типа узла на кнопку"  
[ImageDraggingNodeTopList]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-reorder-dom-nodes.msft.png "Рисунок 12: перетаскивание узла в верхнюю часть списка"  
[ImageNodeDomTreeAfterHidden]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-hide-a-node.msft.png "Рис. 13: вид узла в дереве DOM после того, как он скрыт"  
[ImageFirstConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png "Рисунок 14: результат первого выражения $0 в консоли"  
[ImageSecondConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png "Рисунок 15: результат второго выражения $0 в консоли"  
[ImageResultTemp1]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png "Рисунок 16: результат выражения temp1"  
[ImageResultCopyJSPath]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png "Рис. 17: результат выражения Copy JS Path"  
[ImageBreakAttributeModification]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png "Рисунок 18: прерывание изменений атрибутов"  
[ImageResumeScript]: /microsoft-edge/devtools-guide-chromium/media/dom-break-attribute-modifications-sources-paused-on.msft.png "На рисунке 19 показано, как возобновить выполнение сценария."  
[ImageNotSeeingAllOptions]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-right-click-right-side.msft.png "Рисунок 20: где щелкнуть, если вы не видите все параметры"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft Edge \ (Chromium \)"  
[DevToolsCssGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  
[DevToolsShortcutsElements]: /microsoft-edge/devtools-guide-chromium/shortcuts#elements-panel-keyboard-shortcuts "Сочетания клавиш для панели элементов — сочетания клавиш в Microsoft Edge DevTools"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Пример Microsoft EDGE (Chromium) DevTools DOM | Цепь"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="cae26-384">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cae26-384">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cae26-385">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/dom/index) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).</span><span class="sxs-lookup"><span data-stu-id="cae26-385">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cae26-387">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cae26-387">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

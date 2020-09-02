---
title: Приступая к просмотру и изменению модели DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 6d41b072a8bd19ae728cc02b43eb2f843d91b332
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991204"
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





# <span data-ttu-id="aa02c-103">Приступая к просмотру и изменению модели DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-103">Get started with viewing and changing the DOM</span></span>   



<span data-ttu-id="aa02c-104">Заполните эти интерактивные учебники, чтобы ознакомиться с основными принципами просмотра и изменения модели DOM на странице с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa02c-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="aa02c-105">В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.</span><span class="sxs-lookup"><span data-stu-id="aa02c-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="aa02c-106">Ознакомьтесь с приложением [: HTML и модель DOM](#appendix-html-versus-the-dom) для объяснения.</span><span class="sxs-lookup"><span data-stu-id="aa02c-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="aa02c-107">Примеры открытых DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-107">Open DOM examples</span></span>  

1.  <span data-ttu-id="aa02c-108">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры DOM** , чтобы открыть ее на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="aa02c-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="aa02c-109">Примеры DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="aa02c-110">Просмотр узлов DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-110">View DOM nodes</span></span>   

<span data-ttu-id="aa02c-111">На панели "элементы" в дереве DOM можно выполнить все действия, связанные с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa02c-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="aa02c-112">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-112">Inspect a node</span></span>   

<span data-ttu-id="aa02c-113">Если вы заинтересованы в определенном узле DOM, **Проверьте** , как быстро открыть DevTools и проанализировать этот узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="aa02c-114">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-115">В разделе **Проверка узла**щелкните правой кнопкой мыши **Michelangelo** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="aa02c-117">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-117">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="aa02c-118">Откроется панель " **элементы** " DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa02c-118">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="aa02c-119">в **дереве DOM**выделено.</span><span class="sxs-lookup"><span data-stu-id="aa02c-119">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Выделение узла Michelangelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="aa02c-121">Выделение `Michelangelo` узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-121">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="aa02c-122">Щелкните значок **проверить** \ ( ![ проверить ][ImageInspectIcon] \) в левом верхнем углу DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa02c-122">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Значок проверки" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="aa02c-124">Значок **проверки**</span><span class="sxs-lookup"><span data-stu-id="aa02c-124">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="aa02c-125">В разделе **Проверка узла**щелкните текст в **Токио** .</span><span class="sxs-lookup"><span data-stu-id="aa02c-125">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="aa02c-126">Теперь `<li>Tokyo</li>` выделена в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-126">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="aa02c-127">Проверка узла также является первым шагом в направлении просмотра и изменения стилей узла.</span><span class="sxs-lookup"><span data-stu-id="aa02c-127">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="aa02c-128">Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="aa02c-128">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="aa02c-129">Навигация по дереву DOM с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="aa02c-129">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="aa02c-130">После того как вы выбрали узел в дереве DOM, вы можете перемещаться по дереву DOM с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="aa02c-130">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="aa02c-131">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-131">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-132">В разделе **Навигация по дереву DOM с помощью клавиатуры**щелкните правой кнопкой мыши **Ringo** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-132">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="aa02c-133">выбрано в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-133">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Проверка узла Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="aa02c-135">Проверка `Ringo` узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-135">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="aa02c-136">Нажимайте клавишу `Up` стрелка 2.</span><span class="sxs-lookup"><span data-stu-id="aa02c-136">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="aa02c-137">.</span><span class="sxs-lookup"><span data-stu-id="aa02c-137">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Проверка узла UL" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="aa02c-139">Проверка `ul` узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-139">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="aa02c-140">Нажмите клавишу `Left` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="aa02c-140">Press the `Left` arrow key.</span></span>  <span data-ttu-id="aa02c-141">`<ul>`Список сворачивается.</span><span class="sxs-lookup"><span data-stu-id="aa02c-141">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="aa02c-142">Снова нажмите клавишу `Left` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="aa02c-142">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="aa02c-143">Выбран родительский элемент `<ul>` узла.</span><span class="sxs-lookup"><span data-stu-id="aa02c-143">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="aa02c-144">В этом случае это `<div>` идентификатор `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-144">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="aa02c-145">Нажимайте клавишу `Down` стрелка 2, чтобы повторно выбрать `<ul>` только что свернутый список.</span><span class="sxs-lookup"><span data-stu-id="aa02c-145">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="aa02c-146">Это должно выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="aa02c-146">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="aa02c-147">Нажмите клавишу `Right` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="aa02c-147">Press the `Right` arrow key.</span></span>  <span data-ttu-id="aa02c-148">Список будет развернут.</span><span class="sxs-lookup"><span data-stu-id="aa02c-148">The list expands.</span></span>  

### <span data-ttu-id="aa02c-149">Прокрутка представления</span><span class="sxs-lookup"><span data-stu-id="aa02c-149">Scroll into view</span></span>   

<span data-ttu-id="aa02c-150">При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в данный момент не находится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="aa02c-150">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="aa02c-151">Например, предположим, что вы прокручивается в нижней части страницы, и вы заинтересованы в `<h1>` узле в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="aa02c-151">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="aa02c-152">**Прокрутка представления** позволяет быстро изменить расположение окна просмотра, чтобы вы могли видеть этот узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-152">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="aa02c-153">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-153">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-154">В разделе **прокрутить представление**щелкните правой кнопкой мыши **Magritte** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-154">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="aa02c-155">Прокрутите страницу "примеры DOM" до конца.</span><span class="sxs-lookup"><span data-stu-id="aa02c-155">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="aa02c-156">Этот `<li>Magritte</li>` узел по-прежнему должен быть выбран в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-156">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="aa02c-157">В противном случае вернитесь на [страницу Просмотр](#scroll-into-view) и начните заново.</span><span class="sxs-lookup"><span data-stu-id="aa02c-157">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="aa02c-158">Щелкните правой кнопкой мыши `<li>Magritte</li>` узел и выберите **прокрутить до представления**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-158">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="aa02c-159">Ваше окно просмотра будет прокручено, чтобы вы могли видеть узел **Magritte** .</span><span class="sxs-lookup"><span data-stu-id="aa02c-159">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="aa02c-160">Если вы не видите параметр **прокрутить в представлении** , вы можете просмотреть [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="aa02c-160">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Прокрутка представления" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="aa02c-162">Прокрутка представления</span><span class="sxs-lookup"><span data-stu-id="aa02c-162">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="aa02c-163">Поиск узлов</span><span class="sxs-lookup"><span data-stu-id="aa02c-163">Search for nodes</span></span>   

<span data-ttu-id="aa02c-164">Вы можете выполнить поиск по дереву DOM по строке, селектору CSS или селектору XPath.</span><span class="sxs-lookup"><span data-stu-id="aa02c-164">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="aa02c-165">Сосредоточьте указатель мыши на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="aa02c-165">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="aa02c-166">Нажмите клавиши `Control` + `F` \ (Windows \) или `Command` + `F` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="aa02c-166">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="aa02c-167">Строка поиска откроется в нижней части дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-167">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="aa02c-168">Введите `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="aa02c-168">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="aa02c-169">Последнее предложение выделено в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-169">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Выделение запроса в строке поиска" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="aa02c-171">Выделение запроса в строке поиска</span><span class="sxs-lookup"><span data-stu-id="aa02c-171">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa02c-172">Как упоминалось выше, строка поиска также поддерживает селекторы CSS и XPath.</span><span class="sxs-lookup"><span data-stu-id="aa02c-172">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="aa02c-173">Редактирование модели DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-173">Edit the DOM</span></span>   

<span data-ttu-id="aa02c-174">Вы можете изменить модель DOM на лету и посмотреть, как эти изменения влияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="aa02c-174">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="aa02c-175">Редактирование контента</span><span class="sxs-lookup"><span data-stu-id="aa02c-175">Edit content</span></span>   

<span data-ttu-id="aa02c-176">Чтобы изменить содержимое узла, дважды щелкните его содержимое в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-176">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="aa02c-177">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-177">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-178">В разделе **изменить содержимое**щелкните правой кнопкой мыши **Мишель** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-178">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-179">В дереве DOM дважды щелкните `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-179">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="aa02c-180">Другими словами, дважды щелкните текст между `<li>` and `</li>` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-180">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="aa02c-181">Текст будет выделено, чтобы показать, что он выделен.</span><span class="sxs-lookup"><span data-stu-id="aa02c-181">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Редактирование текста" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="aa02c-183">Редактирование текста</span><span class="sxs-lookup"><span data-stu-id="aa02c-183">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="aa02c-184">Удалить `Michelle` , введите `Leela` и нажмите кнопку, `Enter` чтобы подтвердить изменение.</span><span class="sxs-lookup"><span data-stu-id="aa02c-184">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="aa02c-185">Текст в DOM изменится с **Мишель** на **Leela**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-185">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="aa02c-186">Изменение атрибутов</span><span class="sxs-lookup"><span data-stu-id="aa02c-186">Edit attributes</span></span>   

<span data-ttu-id="aa02c-187">Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="aa02c-187">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="aa02c-188">Следуйте инструкциям, чтобы научиться добавлять атрибуты на узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-188">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="aa02c-189">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-189">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-190">В разделе **изменить атрибуты**щелкните правой кнопкой мыши **Говард** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-190">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="aa02c-191">Дважды щелкните `<li>` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-191">Double-click `<li>`.</span></span>  <span data-ttu-id="aa02c-192">Текст будет выделено, чтобы показать, что выбран узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-192">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Изменение узла" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="aa02c-194">Изменение узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-194">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa02c-195">Нажимайте клавишу `Right` со стрелкой, добавьте пробел, введите текст `style="background-color:gold"` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-195">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="aa02c-196">Цвет фона узла изменится на Золотой.</span><span class="sxs-lookup"><span data-stu-id="aa02c-196">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Добавление атрибута стиля на узел" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="aa02c-198">Добавление `style` атрибута на узел</span><span class="sxs-lookup"><span data-stu-id="aa02c-198">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="aa02c-199">Изменить тип узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-199">Edit node type</span></span>   

<span data-ttu-id="aa02c-200">Чтобы изменить тип узла, дважды щелкните его, а затем введите новый тип.</span><span class="sxs-lookup"><span data-stu-id="aa02c-200">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="aa02c-201">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-201">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-202">В разделе **изменить тип узла**щелкните правой кнопкой мыши **Hank** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-202">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-203">Дважды щелкните `<li>` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-203">Double-click `<li>`.</span></span>  <span data-ttu-id="aa02c-204">Текст `li` будет выделен.</span><span class="sxs-lookup"><span data-stu-id="aa02c-204">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="aa02c-205">Удалить `li` , введите `button` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-205">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="aa02c-206">`<li>`Узел изменится на `<button>` узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-206">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Изменение типа узла на кнопку" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="aa02c-208">Измените тип узла на</span><span class="sxs-lookup"><span data-stu-id="aa02c-208">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="aa02c-209">Изменение порядка узлов DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-209">Reorder DOM nodes</span></span>   

<span data-ttu-id="aa02c-210">Перетащите узлы, чтобы изменить их порядок.</span><span class="sxs-lookup"><span data-stu-id="aa02c-210">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="aa02c-211">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-212">В разделе **изменение порядка узлов DOM**щелкните **Elvis Presley** правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-212">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="aa02c-213">Это последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="aa02c-213">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="aa02c-214">В дереве DOM перетащите указатель `<li>Elvis Presley</li>` в верхнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="aa02c-214">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Перетащите узел в верхнюю часть списка." lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="aa02c-216">Перетащите узел в верхнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="aa02c-216">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="aa02c-217">Принудительное состояние</span><span class="sxs-lookup"><span data-stu-id="aa02c-217">Force state</span></span>   

<span data-ttu-id="aa02c-218">Вы можете принудительно оставлять узлы в состоянии, в том числе,,, `:active` `:hover` `:focus` `:visited` и `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-218">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="aa02c-219">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-219">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-220">В разделе **принудительное состояние**наведите указатель мыши на **Lord летит**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-220">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="aa02c-221">Цвет фона становится оранжевым.</span><span class="sxs-lookup"><span data-stu-id="aa02c-221">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="aa02c-222">Щелкните **Lord летит** правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-222">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-223">Щелкните правой кнопкой мыши `<li class="demo--hover">The Lord of the Flies</li>` и выберите **принудительное состояние**  >  **: наведение**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-223">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="aa02c-224">Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="aa02c-224">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="aa02c-225">Цвет фона остается оранжевым, несмотря на то что вы не наводите указатель мыши на узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-225">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="aa02c-226">Скрытие узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-226">Hide a node</span></span>   

<span data-ttu-id="aa02c-227">Нажмите `H` , чтобы скрыть узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-227">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="aa02c-228">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-228">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-229">В разделе **скрыть узел**щелкните правой кнопкой мыши **звезду назначения** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-229">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-230">Нажмите клавишу `H` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-230">Press the `H` key.</span></span>  <span data-ttu-id="aa02c-231">Узел скрыт.</span><span class="sxs-lookup"><span data-stu-id="aa02c-231">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Как выглядит узел в дереве DOM после его скрытия" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="aa02c-233">Как выглядит узел в дереве DOM после его скрытия</span><span class="sxs-lookup"><span data-stu-id="aa02c-233">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="aa02c-234">Снова нажмите клавишу `H` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-234">Press the `H` key again.</span></span>  <span data-ttu-id="aa02c-235">Узел снова появится.</span><span class="sxs-lookup"><span data-stu-id="aa02c-235">The node is shown again.</span></span>  

### <span data-ttu-id="aa02c-236">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-236">Delete a node</span></span>   

<span data-ttu-id="aa02c-237">Нажмите `Delete` , чтобы удалить узел.</span><span class="sxs-lookup"><span data-stu-id="aa02c-237">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="aa02c-238">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-238">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-239">В разделе **Удаление узла**щелкните правой кнопкой мыши элемент **Foundation** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-239">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-240">Нажмите клавишу `Delete` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-240">Press the `Delete` key.</span></span>  <span data-ttu-id="aa02c-241">Узел удален.</span><span class="sxs-lookup"><span data-stu-id="aa02c-241">The node is deleted.</span></span>  
    1.  <span data-ttu-id="aa02c-242">Нажмите клавиши `Control` + `Z` \ (Windows \) или `Command` + `Z` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="aa02c-242">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="aa02c-243">Последнее действие отменено, и узел появится снова.</span><span class="sxs-lookup"><span data-stu-id="aa02c-243">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="aa02c-244">Узлы Access на консоли</span><span class="sxs-lookup"><span data-stu-id="aa02c-244">Access nodes in the Console</span></span>   

<span data-ttu-id="aa02c-245">DevTools предоставляет несколько сочетаний клавиш для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждую из них.</span><span class="sxs-lookup"><span data-stu-id="aa02c-245">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="aa02c-246">Ссылка на узел, выбранный в настоящее время с помощью $0</span><span class="sxs-lookup"><span data-stu-id="aa02c-246">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="aa02c-247">Когда вы просматриваете узел, `== $0` текст рядом с узлом означает, что вы можете добавить ссылку на этот узел в консоль с переменной `$0` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-247">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="aa02c-248">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-248">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-249">В разделе **ссылка на узел, выбранный в $0**, щелкните правой кнопкой мыши **в левой части экрана** , а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-249">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-250">Нажмите клавишу, `Escape` чтобы открыть консольный ящик.</span><span class="sxs-lookup"><span data-stu-id="aa02c-250">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="aa02c-251">Введите текст и нажмите клавишу ВВОД `$0` `Enter` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-251">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="aa02c-252">Результат выражения показывает, что выражение `$0` имеет значение `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-252">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Результат первого выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="aa02c-254">Результат первого `$0` выражения в **консоли**</span><span class="sxs-lookup"><span data-stu-id="aa02c-254">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="aa02c-255">Наведите указатель мыши на результат.</span><span class="sxs-lookup"><span data-stu-id="aa02c-255">Hover over the result.</span></span>  <span data-ttu-id="aa02c-256">Узел выделится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="aa02c-256">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="aa02c-257">Щелкните `<li>Dune</li>` дерево DOM, введите `$0` консоль еще раз, а затем нажмите `Enter` еще раз.</span><span class="sxs-lookup"><span data-stu-id="aa02c-257">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="aa02c-258">Теперь `$0` оценивается `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-258">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Результат второго выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="aa02c-260">Результат второго `$0` выражения в **консоли**</span><span class="sxs-lookup"><span data-stu-id="aa02c-260">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="aa02c-261">Сохранить как глобальную переменную</span><span class="sxs-lookup"><span data-stu-id="aa02c-261">Store as global variable</span></span>   

<span data-ttu-id="aa02c-262">Если необходимо повторно сослаться на узел, сохраните его как глобальную переменную.</span><span class="sxs-lookup"><span data-stu-id="aa02c-262">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="aa02c-263">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-263">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-264">В разделе **Сохранить как глобальную переменную**щелкните правой кнопкой мыши **в большом спящем режиме** и выберите **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-264">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-265">Щелкните правой кнопкой мыши `<li>The Big Sleep</li>` дерево DOM и выберите **Сохранить как глобальную переменную**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-265">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="aa02c-266">Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="aa02c-266">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="aa02c-267">Введите текст `temp1` на консоли и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-267">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="aa02c-268">Результат выражения показывает, что переменная является узлом.</span><span class="sxs-lookup"><span data-stu-id="aa02c-268">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Результат выражения temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="aa02c-270">Результат `temp1` выражения</span><span class="sxs-lookup"><span data-stu-id="aa02c-270">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="aa02c-271">Скопировать путь к JS</span><span class="sxs-lookup"><span data-stu-id="aa02c-271">Copy JS path</span></span>   

<span data-ttu-id="aa02c-272">Скопируйте путь JavaScript на узел, если вам нужно сослаться на него в автоматическом тесте.</span><span class="sxs-lookup"><span data-stu-id="aa02c-272">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="aa02c-273">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-273">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-274">В разделе **скопировать путь к каталогу**щелкните правой кнопкой мыши **братьев Karamazov** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-274">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-275">Щелкните правой кнопкой мыши `<li>The Brothers Karamazov</li>` дерево DOM и выберите команду **Копировать**  >  **путь к каталогу**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-275">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="aa02c-276">`document.querySelector()`Выражение, которое разрешается в узел, копируется в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="aa02c-276">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="aa02c-277">`Control` + `V` Чтобы вставить выражение на консоль, нажмите клавиши \ (Windows \) или `Command` + `V` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="aa02c-277">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="aa02c-278">Нажмите `Enter` , чтобы вычислить выражение.</span><span class="sxs-lookup"><span data-stu-id="aa02c-278">Press `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Результат выражения Copy JS Path" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="aa02c-280">Результат выражения **Copy JS Path**</span><span class="sxs-lookup"><span data-stu-id="aa02c-280">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="aa02c-281">Прерывание изменений DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-281">Break on DOM changes</span></span>   

<span data-ttu-id="aa02c-282">DevTools позволяет приостановить JavaScript на странице, когда JavaScript изменит модель DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-282">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="aa02c-283">Прерывание изменений атрибутов</span><span class="sxs-lookup"><span data-stu-id="aa02c-283">Break on attribute modifications</span></span>   

<span data-ttu-id="aa02c-284">Используйте точки останова по изменению атрибутов, если требуется приостановить JavaScript, который приводит к изменению любого атрибута узла.</span><span class="sxs-lookup"><span data-stu-id="aa02c-284">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="aa02c-285">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-285">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-286">В разделе **прервать на странице "изменения атрибутов**" щелкните правой кнопкой мыши **Sauerkraut** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-286">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-287">В дереве DOM щелкните правой кнопкой мыши `<li id="target">Sauerkraut</li>` и выберите команду **прервать для**  >  **изменений атрибутов**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-287">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="aa02c-288">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="aa02c-288">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Прерывание изменений атрибутов" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="aa02c-290">Прерывание изменений атрибутов</span><span class="sxs-lookup"><span data-stu-id="aa02c-290">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="aa02c-291">На следующем этапе вы будете получать инструкции по нажатию кнопки, которая приостанавливает код страницы.</span><span class="sxs-lookup"><span data-stu-id="aa02c-291">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="aa02c-292">После того как страница приостановлена, прокрутка страницы больше недоступна.</span><span class="sxs-lookup"><span data-stu-id="aa02c-292">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="aa02c-293">**Resume Script** ![ ][ImageResumeScriptIcon] Чтобы снова выполнить прокрутку страницы, необходимо нажать кнопку возобновить сценарий \ (возобновить сценарий \).</span><span class="sxs-lookup"><span data-stu-id="aa02c-293">You must click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Как возобновить выполнение сценария" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="aa02c-295">Как возобновить выполнение сценария</span><span class="sxs-lookup"><span data-stu-id="aa02c-295">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="aa02c-296">Нажмите кнопку " **настроить фон** ".</span><span class="sxs-lookup"><span data-stu-id="aa02c-296">Click the **Set Background** button above.</span></span>  <span data-ttu-id="aa02c-297">Таким образом, `style` для атрибута узла будет задано значение `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="aa02c-297">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="aa02c-298">DevTools приостанавливает страницу и выделяет код, который привел к изменению атрибута.</span><span class="sxs-lookup"><span data-stu-id="aa02c-298">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="aa02c-299">Нажмите кнопку **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \), как упоминалось ранее.</span><span class="sxs-lookup"><span data-stu-id="aa02c-299">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="aa02c-300">Прерывание при удалении узла</span><span class="sxs-lookup"><span data-stu-id="aa02c-300">Break on node removal</span></span>   

<span data-ttu-id="aa02c-301">Если вы хотите приостановить работу при удалении определенного узла, используйте точки останова удаления узла.</span><span class="sxs-lookup"><span data-stu-id="aa02c-301">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="aa02c-302">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-302">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-303">В разделе **прервать удаление узла**щелкните правой кнопкой мыши **Neuromancer** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-303">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-304">В дереве DOM щелкните правой кнопкой мыши `<li id="target">Neuromancer</li>` и выберите команду **прервать при**  >  **удалении узла**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-304">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="aa02c-305">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="aa02c-305">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="aa02c-306">Нажмите кнопку " **Удалить** ".</span><span class="sxs-lookup"><span data-stu-id="aa02c-306">Click the **Delete** button above.</span></span>  <span data-ttu-id="aa02c-307">DevTools приостанавливает страницу и выделяет код, вызвавший удаление узла.</span><span class="sxs-lookup"><span data-stu-id="aa02c-307">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="aa02c-308">Нажмите кнопку **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa02c-308">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="aa02c-309">Прерывание при изменении поддерева</span><span class="sxs-lookup"><span data-stu-id="aa02c-309">Break on subtree modifications</span></span>   

<span data-ttu-id="aa02c-310">После того как вы добавите на узел точку останова изменения поддерева, DevTools приостанавливает страницу при добавлении или удалении любого потомка узла.</span><span class="sxs-lookup"><span data-stu-id="aa02c-310">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="aa02c-311">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="aa02c-311">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="aa02c-312">В разделе **прервать при изменении поддерева**щелкните правой кнопкой мыши значок **Fire** и выберите пункт **проверить**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-312">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="aa02c-313">В дереве DOM щелкните правой кнопкой мыши расположенный `<ul id="target">` выше узел `<li>A Fire Upon the Deep</li>` и выберите команду **приостановить**  >  **изменение поддерева**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-313">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="aa02c-314">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="aa02c-314">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="aa02c-315">Нажмите кнопку **Добавить ребенка**.</span><span class="sxs-lookup"><span data-stu-id="aa02c-315">Click **Add Child**.</span></span>  <span data-ttu-id="aa02c-316">Код приостанавливается, так как `<li>` узел был добавлен в список.</span><span class="sxs-lookup"><span data-stu-id="aa02c-316">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="aa02c-317">Нажмите кнопку **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa02c-317">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="aa02c-318">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="aa02c-318">Next steps</span></span>   

<span data-ttu-id="aa02c-319">, Которая охватывает большую часть функций, связанных с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa02c-319">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="aa02c-320">Вы можете найти остальные элементы, щелкнув правой кнопкой мыши узлы в дереве DOM и экспериментируя с другими параметрами, которые не были рассмотрены в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="aa02c-320">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="aa02c-321">Вы также можете просмотреть [сочетания клавиш для панели элементов][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="aa02c-321">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="aa02c-322">Ознакомьтесь с [домашней страницей Microsoft Edge DevTools][MicrosoftEdgeDevTools] , чтобы найти все, что вы можете делать с DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa02c-322">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="aa02c-323">Приложение: HTML и модель DOM</span><span class="sxs-lookup"><span data-stu-id="aa02c-323">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="aa02c-324">В следующем разделе показано, как быстро рассказано о различиях между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-324">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="aa02c-325">При использовании веб-браузера для запроса страницы сервер возвращает HTML-код, как в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="aa02c-325">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="aa02c-326">Браузер анализирует HTML и создает дерево объектов, как в приведенном ниже списке.</span><span class="sxs-lookup"><span data-stu-id="aa02c-326">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="aa02c-327">Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-327">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="aa02c-328">Теперь оно выглядит так же, как HTML, но предположим, что сценарий, указанный в нижней части HTML, выполняет следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="aa02c-328">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="aa02c-329">Этот код удаляет `h1` узел и добавляет еще один `p` узел в модель DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-329">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="aa02c-330">Теперь в качестве полного DOM появится следующий список.</span><span class="sxs-lookup"><span data-stu-id="aa02c-330">The complete DOM now displays the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="aa02c-331">HTML-код страницы теперь отличается от модели DOM.</span><span class="sxs-lookup"><span data-stu-id="aa02c-331">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="aa02c-332">Другими словами, HTML представляет начальное содержимое страницы, а модель DOM — текущее содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="aa02c-332">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="aa02c-333">Когда JavaScript добавляет, удаляет или редактирует узлы, модель DOM становится отличной от HTML.</span><span class="sxs-lookup"><span data-stu-id="aa02c-333">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="aa02c-334">Дополнительные сведения можно найти в разделе [Введение в модель DOM][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="aa02c-334">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
   Scroll into view  
:::image-end:::  
    -->  

## <span data-ttu-id="aa02c-335">Приложение: отсутствующие параметры</span><span class="sxs-lookup"><span data-stu-id="aa02c-335">Appendix: Missing options</span></span>   

<span data-ttu-id="aa02c-336">Многие инструкции, описанные в этом руководстве, помогут вам щелкнуть правой кнопкой мыши узел в дереве DOM и выбрать нужный вариант в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="aa02c-336">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="aa02c-337">Если указанный параметр не отображается в контекстном меню, попробуйте щелкнуть правой кнопкой мыши за пределами текста узла.</span><span class="sxs-lookup"><span data-stu-id="aa02c-337">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Выбор варианта, если вы не видите все параметры" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="aa02c-339">Выбор варианта, если вы не видите все параметры</span><span class="sxs-lookup"><span data-stu-id="aa02c-339">Where to click if you are not seeing all the options</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chromium \) Инструменты разработчика | Документы Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Сочетания клавиш для панели элементов — сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Пример Microsoft EDGE (Chromium) DevTools DOM | Цепь"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="aa02c-345">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa02c-345">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aa02c-346">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/dom/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="aa02c-346">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aa02c-348">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa02c-348">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

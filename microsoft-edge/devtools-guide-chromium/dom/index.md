---
description: Инструкции по просмотру узлов, поиску узлов, изменению узлов, узлам ссылок в консоли, прерыванию изменений узла и т. д.
title: Приступая к просмотру и изменению модели DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 555e627b70f0cc5e50c0676cf90067c2709a9ae3
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992955"
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





# <span data-ttu-id="50ce6-104">Приступая к просмотру и изменению модели DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-104">Get started with viewing and changing the DOM</span></span>   



<span data-ttu-id="50ce6-105">Заполните эти интерактивные учебники, чтобы ознакомиться с основными принципами просмотра и изменения модели DOM на странице с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="50ce6-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="50ce6-106">В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.</span><span class="sxs-lookup"><span data-stu-id="50ce6-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="50ce6-107">Ознакомьтесь с приложением [: HTML и модель DOM](#appendix-html-versus-the-dom) для объяснения.</span><span class="sxs-lookup"><span data-stu-id="50ce6-107">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="50ce6-108">Примеры открытых DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="50ce6-109">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры DOM** , чтобы открыть ее на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="50ce6-109">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="50ce6-110">Примеры DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="50ce6-111">Просмотр узлов DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-111">View DOM nodes</span></span>   

<span data-ttu-id="50ce6-112">На панели "элементы" в дереве DOM можно выполнить все действия, связанные с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="50ce6-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="50ce6-113">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-113">Inspect a node</span></span>   

<span data-ttu-id="50ce6-114">Если вы заинтересованы в определенном узле DOM, **Проверьте** , как быстро открыть DevTools и проанализировать этот узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="50ce6-115">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-116">В разделе **Проверка узла**щелкните правой кнопкой мыши **Michelangelo** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-116">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="50ce6-118">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="50ce6-119">Откроется панель " **элементы** " DevTools.</span><span class="sxs-lookup"><span data-stu-id="50ce6-119">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="50ce6-120">в **дереве DOM**выделено.</span><span class="sxs-lookup"><span data-stu-id="50ce6-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Выделение узла Michelangelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="50ce6-122">Выделение `Michelangelo` узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="50ce6-123">Щелкните значок **проверить** \ ( ![ проверить ][ImageInspectIcon] \) в левом верхнем углу DevTools.</span><span class="sxs-lookup"><span data-stu-id="50ce6-123">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Значок проверки" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="50ce6-125">Значок **проверки**</span><span class="sxs-lookup"><span data-stu-id="50ce6-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="50ce6-126">В разделе **Проверка узла**щелкните текст в **Токио** .</span><span class="sxs-lookup"><span data-stu-id="50ce6-126">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="50ce6-127">Теперь `<li>Tokyo</li>` выделена в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="50ce6-128">Проверка узла также является первым шагом в направлении просмотра и изменения стилей узла.</span><span class="sxs-lookup"><span data-stu-id="50ce6-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="50ce6-129">Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="50ce6-129">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="50ce6-130">Навигация по дереву DOM с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="50ce6-130">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="50ce6-131">После того как вы выбрали узел в дереве DOM, вы можете перемещаться по дереву DOM с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="50ce6-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="50ce6-132">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-133">В разделе **Навигация по дереву DOM с помощью клавиатуры**щелкните правой кнопкой мыши **Ringo** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-133">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="50ce6-134">выбрано в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Проверка узла Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="50ce6-136">Проверка `Ringo` узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="50ce6-137">Нажимайте клавишу `Up` стрелка 2.</span><span class="sxs-lookup"><span data-stu-id="50ce6-137">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="50ce6-138">.</span><span class="sxs-lookup"><span data-stu-id="50ce6-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Проверка узла UL" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="50ce6-140">Проверка `ul` узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="50ce6-141">Нажмите клавишу `Left` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="50ce6-141">Press the `Left` arrow key.</span></span>  <span data-ttu-id="50ce6-142">`<ul>`Список сворачивается.</span><span class="sxs-lookup"><span data-stu-id="50ce6-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="50ce6-143">Снова нажмите клавишу `Left` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="50ce6-143">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="50ce6-144">Выбран родительский элемент `<ul>` узла.</span><span class="sxs-lookup"><span data-stu-id="50ce6-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="50ce6-145">В этом случае это `<div>` идентификатор `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="50ce6-146">Нажимайте клавишу `Down` стрелка 2, чтобы повторно выбрать `<ul>` только что свернутый список.</span><span class="sxs-lookup"><span data-stu-id="50ce6-146">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="50ce6-147">Это должно выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="50ce6-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="50ce6-148">Нажмите клавишу `Right` со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="50ce6-148">Press the `Right` arrow key.</span></span>  <span data-ttu-id="50ce6-149">Список будет развернут.</span><span class="sxs-lookup"><span data-stu-id="50ce6-149">The list expands.</span></span>  

### <span data-ttu-id="50ce6-150">Прокрутка представления</span><span class="sxs-lookup"><span data-stu-id="50ce6-150">Scroll into view</span></span>   

<span data-ttu-id="50ce6-151">При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в данный момент не находится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="50ce6-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="50ce6-152">Например, предположим, что вы прокручивается в нижней части страницы, и вы заинтересованы в `<h1>` узле в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="50ce6-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="50ce6-153">**Прокрутка представления** позволяет быстро изменить расположение окна просмотра, чтобы вы могли видеть этот узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="50ce6-154">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-155">В разделе **прокрутить представление**щелкните правой кнопкой мыши **Magritte** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-155">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="50ce6-156">Прокрутите страницу "примеры DOM" до конца.</span><span class="sxs-lookup"><span data-stu-id="50ce6-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="50ce6-157">Этот `<li>Magritte</li>` узел по-прежнему должен быть выбран в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="50ce6-158">В противном случае вернитесь на [страницу Просмотр](#scroll-into-view) и начните заново.</span><span class="sxs-lookup"><span data-stu-id="50ce6-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="50ce6-159">Щелкните правой кнопкой мыши `<li>Magritte</li>` узел и выберите **прокрутить до представления**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-159">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="50ce6-160">Ваше окно просмотра будет прокручено, чтобы вы могли видеть узел **Magritte** .</span><span class="sxs-lookup"><span data-stu-id="50ce6-160">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="50ce6-161">Если вы не видите параметр **прокрутить в представлении** , вы можете просмотреть [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="50ce6-161">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Прокрутка представления" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="50ce6-163">Прокрутка представления</span><span class="sxs-lookup"><span data-stu-id="50ce6-163">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="50ce6-164">Поиск узлов</span><span class="sxs-lookup"><span data-stu-id="50ce6-164">Search for nodes</span></span>   

<span data-ttu-id="50ce6-165">Вы можете выполнить поиск по дереву DOM по строке, селектору CSS или селектору XPath.</span><span class="sxs-lookup"><span data-stu-id="50ce6-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="50ce6-166">Сосредоточьте указатель мыши на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="50ce6-166">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="50ce6-167">Нажмите клавиши `Control` + `F` \ (Windows \) или `Command` + `F` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="50ce6-167">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="50ce6-168">Строка поиска откроется в нижней части дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="50ce6-169">Введите `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="50ce6-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="50ce6-170">Последнее предложение выделено в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Выделение запроса в строке поиска" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="50ce6-172">Выделение запроса в строке поиска</span><span class="sxs-lookup"><span data-stu-id="50ce6-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="50ce6-173">Как упоминалось выше, строка поиска также поддерживает селекторы CSS и XPath.</span><span class="sxs-lookup"><span data-stu-id="50ce6-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="50ce6-174">Редактирование модели DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-174">Edit the DOM</span></span>   

<span data-ttu-id="50ce6-175">Вы можете изменить модель DOM на лету и посмотреть, как эти изменения влияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="50ce6-175">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="50ce6-176">Редактирование контента</span><span class="sxs-lookup"><span data-stu-id="50ce6-176">Edit content</span></span>   

<span data-ttu-id="50ce6-177">Чтобы изменить содержимое узла, дважды щелкните его содержимое в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="50ce6-178">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-179">В разделе **изменить содержимое**щелкните правой кнопкой мыши **Мишель** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-179">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-180">В дереве DOM дважды щелкните `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="50ce6-181">Другими словами, дважды щелкните текст между `<li>` and `</li>` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="50ce6-182">Текст будет выделено, чтобы показать, что он выделен.</span><span class="sxs-lookup"><span data-stu-id="50ce6-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Редактирование текста" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="50ce6-184">Редактирование текста</span><span class="sxs-lookup"><span data-stu-id="50ce6-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="50ce6-185">Удалить `Michelle` , введите `Leela` и нажмите кнопку, `Enter` чтобы подтвердить изменение.</span><span class="sxs-lookup"><span data-stu-id="50ce6-185">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="50ce6-186">Текст в DOM изменится с **Мишель** на **Leela**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="50ce6-187">Изменение атрибутов</span><span class="sxs-lookup"><span data-stu-id="50ce6-187">Edit attributes</span></span>   

<span data-ttu-id="50ce6-188">Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="50ce6-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="50ce6-189">Следуйте инструкциям, чтобы научиться добавлять атрибуты на узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="50ce6-190">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-191">В разделе **изменить атрибуты**щелкните правой кнопкой мыши **Говард** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-191">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="50ce6-192">Дважды щелкните `<li>` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-192">Double-click `<li>`.</span></span>  <span data-ttu-id="50ce6-193">Текст будет выделено, чтобы показать, что выбран узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Изменение узла" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="50ce6-195">Изменение узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50ce6-196">Нажимайте клавишу `Right` со стрелкой, добавьте пробел, введите текст `style="background-color:gold"` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-196">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="50ce6-197">Цвет фона узла изменится на Золотой.</span><span class="sxs-lookup"><span data-stu-id="50ce6-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Добавление атрибута стиля на узел" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="50ce6-199">Добавление `style` атрибута на узел</span><span class="sxs-lookup"><span data-stu-id="50ce6-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="50ce6-200">Изменить тип узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-200">Edit node type</span></span>   

<span data-ttu-id="50ce6-201">Чтобы изменить тип узла, дважды щелкните его, а затем введите новый тип.</span><span class="sxs-lookup"><span data-stu-id="50ce6-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="50ce6-202">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-203">В разделе **изменить тип узла**щелкните правой кнопкой мыши **Hank** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-203">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-204">Дважды щелкните `<li>` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-204">Double-click `<li>`.</span></span>  <span data-ttu-id="50ce6-205">Текст `li` будет выделен.</span><span class="sxs-lookup"><span data-stu-id="50ce6-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="50ce6-206">Удалить `li` , введите `button` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-206">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="50ce6-207">`<li>`Узел изменится на `<button>` узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Изменение типа узла на кнопку" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="50ce6-209">Измените тип узла на</span><span class="sxs-lookup"><span data-stu-id="50ce6-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="50ce6-210">Изменение порядка узлов DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-210">Reorder DOM nodes</span></span>   

<span data-ttu-id="50ce6-211">Перетащите узлы, чтобы изменить их порядок.</span><span class="sxs-lookup"><span data-stu-id="50ce6-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="50ce6-212">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-213">В разделе **изменение порядка узлов DOM**щелкните **Elvis Presley** правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-213">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="50ce6-214">Это последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="50ce6-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="50ce6-215">В дереве DOM перетащите указатель `<li>Elvis Presley</li>` в верхнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="50ce6-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Перетащите узел в верхнюю часть списка." lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="50ce6-217">Перетащите узел в верхнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="50ce6-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="50ce6-218">Принудительное состояние</span><span class="sxs-lookup"><span data-stu-id="50ce6-218">Force state</span></span>   

<span data-ttu-id="50ce6-219">Вы можете принудительно оставлять узлы в состоянии, в том числе,,, `:active` `:hover` `:focus` `:visited` и `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="50ce6-220">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-221">В разделе **принудительное состояние**наведите указатель мыши на **Lord летит**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-221">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="50ce6-222">Цвет фона становится оранжевым.</span><span class="sxs-lookup"><span data-stu-id="50ce6-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="50ce6-223">Щелкните **Lord летит** правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-223">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-224">Щелкните правой кнопкой мыши `<li class="demo--hover">The Lord of the Flies</li>` и выберите **принудительное состояние**  >  **: наведение**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-224">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="50ce6-225">Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="50ce6-225">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="50ce6-226">Цвет фона остается оранжевым, несмотря на то что вы не наводите указатель мыши на узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="50ce6-227">Скрытие узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-227">Hide a node</span></span>   

<span data-ttu-id="50ce6-228">Нажмите `H` , чтобы скрыть узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-228">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="50ce6-229">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-230">В разделе **скрыть узел**щелкните правой кнопкой мыши **звезду назначения** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-230">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-231">Нажмите клавишу `H` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-231">Press the `H` key.</span></span>  <span data-ttu-id="50ce6-232">Узел скрыт.</span><span class="sxs-lookup"><span data-stu-id="50ce6-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Как выглядит узел в дереве DOM после его скрытия" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="50ce6-234">Как выглядит узел в дереве DOM после его скрытия</span><span class="sxs-lookup"><span data-stu-id="50ce6-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="50ce6-235">Снова нажмите клавишу `H` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-235">Press the `H` key again.</span></span>  <span data-ttu-id="50ce6-236">Узел снова появится.</span><span class="sxs-lookup"><span data-stu-id="50ce6-236">The node is shown again.</span></span>  

### <span data-ttu-id="50ce6-237">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-237">Delete a node</span></span>   

<span data-ttu-id="50ce6-238">Нажмите `Delete` , чтобы удалить узел.</span><span class="sxs-lookup"><span data-stu-id="50ce6-238">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="50ce6-239">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-240">В разделе **Удаление узла**щелкните правой кнопкой мыши элемент **Foundation** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-240">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-241">Нажмите клавишу `Delete` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-241">Press the `Delete` key.</span></span>  <span data-ttu-id="50ce6-242">Узел удален.</span><span class="sxs-lookup"><span data-stu-id="50ce6-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="50ce6-243">Нажмите клавиши `Control` + `Z` \ (Windows \) или `Command` + `Z` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="50ce6-243">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="50ce6-244">Последнее действие отменено, и узел появится снова.</span><span class="sxs-lookup"><span data-stu-id="50ce6-244">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="50ce6-245">Узлы Access на консоли</span><span class="sxs-lookup"><span data-stu-id="50ce6-245">Access nodes in the Console</span></span>   

<span data-ttu-id="50ce6-246">DevTools предоставляет несколько сочетаний клавиш для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждую из них.</span><span class="sxs-lookup"><span data-stu-id="50ce6-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="50ce6-247">Ссылка на узел, выбранный в настоящее время с помощью $0</span><span class="sxs-lookup"><span data-stu-id="50ce6-247">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="50ce6-248">Когда вы просматриваете узел, `== $0` текст рядом с узлом означает, что вы можете добавить ссылку на этот узел в консоль с переменной `$0` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="50ce6-249">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-250">В разделе **ссылка на узел, выбранный в $0**, щелкните правой кнопкой мыши **в левой части экрана** , а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-250">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-251">Нажмите клавишу, `Escape` чтобы открыть консольный ящик.</span><span class="sxs-lookup"><span data-stu-id="50ce6-251">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="50ce6-252">Введите текст и нажмите клавишу ВВОД `$0` `Enter` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-252">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="50ce6-253">Результат выражения показывает, что выражение `$0` имеет значение `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Результат первого выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="50ce6-255">Результат первого `$0` выражения в **консоли**</span><span class="sxs-lookup"><span data-stu-id="50ce6-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="50ce6-256">Наведите указатель мыши на результат.</span><span class="sxs-lookup"><span data-stu-id="50ce6-256">Hover over the result.</span></span>  <span data-ttu-id="50ce6-257">Узел выделится в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="50ce6-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="50ce6-258">Щелкните `<li>Dune</li>` дерево DOM, введите `$0` консоль еще раз, а затем нажмите `Enter` еще раз.</span><span class="sxs-lookup"><span data-stu-id="50ce6-258">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="50ce6-259">Теперь `$0` оценивается `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Результат второго выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="50ce6-261">Результат второго `$0` выражения в **консоли**</span><span class="sxs-lookup"><span data-stu-id="50ce6-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="50ce6-262">Сохранить как глобальную переменную</span><span class="sxs-lookup"><span data-stu-id="50ce6-262">Store as global variable</span></span>   

<span data-ttu-id="50ce6-263">Если необходимо повторно сослаться на узел, сохраните его как глобальную переменную.</span><span class="sxs-lookup"><span data-stu-id="50ce6-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="50ce6-264">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-265">В разделе **Сохранить как глобальную переменную**щелкните правой кнопкой мыши **в большом спящем режиме** и выберите **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-265">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-266">Щелкните правой кнопкой мыши `<li>The Big Sleep</li>` дерево DOM и выберите **Сохранить как глобальную переменную**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-266">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="50ce6-267">Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="50ce6-267">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="50ce6-268">Введите текст `temp1` на консоли и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-268">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="50ce6-269">Результат выражения показывает, что переменная является узлом.</span><span class="sxs-lookup"><span data-stu-id="50ce6-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Результат выражения temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="50ce6-271">Результат `temp1` выражения</span><span class="sxs-lookup"><span data-stu-id="50ce6-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="50ce6-272">Скопировать путь к JS</span><span class="sxs-lookup"><span data-stu-id="50ce6-272">Copy JS path</span></span>   

<span data-ttu-id="50ce6-273">Скопируйте путь JavaScript на узел, если вам нужно сослаться на него в автоматическом тесте.</span><span class="sxs-lookup"><span data-stu-id="50ce6-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="50ce6-274">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-275">В разделе **скопировать путь к каталогу**щелкните правой кнопкой мыши **братьев Karamazov** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-275">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-276">Щелкните правой кнопкой мыши `<li>The Brothers Karamazov</li>` дерево DOM и выберите команду **Копировать**  >  **путь к каталогу**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-276">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="50ce6-277">`document.querySelector()`Выражение, которое разрешается в узел, копируется в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="50ce6-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="50ce6-278">`Control` + `V` Чтобы вставить выражение на консоль, нажмите клавиши \ (Windows \) или `Command` + `V` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="50ce6-278">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="50ce6-279">Нажмите `Enter` , чтобы вычислить выражение.</span><span class="sxs-lookup"><span data-stu-id="50ce6-279">Press `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Результат выражения Copy JS Path" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="50ce6-281">Результат выражения **Copy JS Path**</span><span class="sxs-lookup"><span data-stu-id="50ce6-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="50ce6-282">Прерывание изменений DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-282">Break on DOM changes</span></span>   

<span data-ttu-id="50ce6-283">DevTools позволяет приостановить JavaScript на странице, когда JavaScript изменит модель DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="50ce6-284">Прерывание изменений атрибутов</span><span class="sxs-lookup"><span data-stu-id="50ce6-284">Break on attribute modifications</span></span>   

<span data-ttu-id="50ce6-285">Используйте точки останова по изменению атрибутов, если требуется приостановить JavaScript, который приводит к изменению любого атрибута узла.</span><span class="sxs-lookup"><span data-stu-id="50ce6-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="50ce6-286">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-287">В разделе **прервать на странице "изменения атрибутов**" щелкните правой кнопкой мыши **Sauerkraut** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-287">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-288">В дереве DOM щелкните правой кнопкой мыши `<li id="target">Sauerkraut</li>` и выберите команду **прервать для**  >  **изменений атрибутов**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-288">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="50ce6-289">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="50ce6-289">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Прерывание изменений атрибутов" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="50ce6-291">Прерывание изменений атрибутов</span><span class="sxs-lookup"><span data-stu-id="50ce6-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="50ce6-292">На следующем этапе вы будете получать инструкции по нажатию кнопки, которая приостанавливает код страницы.</span><span class="sxs-lookup"><span data-stu-id="50ce6-292">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="50ce6-293">После того как страница приостановлена, прокрутка страницы больше недоступна.</span><span class="sxs-lookup"><span data-stu-id="50ce6-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="50ce6-294">**Resume Script** ![ ][ImageResumeScriptIcon] Чтобы снова выполнить прокрутку страницы, необходимо нажать кнопку возобновить сценарий \ (возобновить сценарий \).</span><span class="sxs-lookup"><span data-stu-id="50ce6-294">You must click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Как возобновить выполнение сценария" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="50ce6-296">Как возобновить выполнение сценария</span><span class="sxs-lookup"><span data-stu-id="50ce6-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="50ce6-297">Нажмите кнопку " **настроить фон** ".</span><span class="sxs-lookup"><span data-stu-id="50ce6-297">Click the **Set Background** button above.</span></span>  <span data-ttu-id="50ce6-298">Таким образом, `style` для атрибута узла будет задано значение `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="50ce6-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="50ce6-299">DevTools приостанавливает страницу и выделяет код, который привел к изменению атрибута.</span><span class="sxs-lookup"><span data-stu-id="50ce6-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="50ce6-300">Нажмите кнопку **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \), как упоминалось ранее.</span><span class="sxs-lookup"><span data-stu-id="50ce6-300">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="50ce6-301">Прерывание при удалении узла</span><span class="sxs-lookup"><span data-stu-id="50ce6-301">Break on node removal</span></span>   

<span data-ttu-id="50ce6-302">Если вы хотите приостановить работу при удалении определенного узла, используйте точки останова удаления узла.</span><span class="sxs-lookup"><span data-stu-id="50ce6-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="50ce6-303">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-304">В разделе **прервать удаление узла**щелкните правой кнопкой мыши **Neuromancer** и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-304">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-305">В дереве DOM щелкните правой кнопкой мыши `<li id="target">Neuromancer</li>` и выберите команду **прервать при**  >  **удалении узла**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-305">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="50ce6-306">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="50ce6-306">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="50ce6-307">Нажмите кнопку " **Удалить** ".</span><span class="sxs-lookup"><span data-stu-id="50ce6-307">Click the **Delete** button above.</span></span>  <span data-ttu-id="50ce6-308">DevTools приостанавливает страницу и выделяет код, вызвавший удаление узла.</span><span class="sxs-lookup"><span data-stu-id="50ce6-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="50ce6-309">Нажмите кнопку **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="50ce6-309">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="50ce6-310">Прерывание при изменении поддерева</span><span class="sxs-lookup"><span data-stu-id="50ce6-310">Break on subtree modifications</span></span>   

<span data-ttu-id="50ce6-311">После того как вы добавите на узел точку останова изменения поддерева, DevTools приостанавливает страницу при добавлении или удалении любого потомка узла.</span><span class="sxs-lookup"><span data-stu-id="50ce6-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="50ce6-312">[Откройте примеры DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="50ce6-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="50ce6-313">В разделе **прервать при изменении поддерева**щелкните правой кнопкой мыши значок **Fire** и выберите пункт **проверить**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-313">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="50ce6-314">В дереве DOM щелкните правой кнопкой мыши расположенный `<ul id="target">` выше узел `<li>A Fire Upon the Deep</li>` и выберите команду **приостановить**  >  **изменение поддерева**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-314">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="50ce6-315">Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .</span><span class="sxs-lookup"><span data-stu-id="50ce6-315">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="50ce6-316">Нажмите кнопку **Добавить ребенка**.</span><span class="sxs-lookup"><span data-stu-id="50ce6-316">Click **Add Child**.</span></span>  <span data-ttu-id="50ce6-317">Код приостанавливается, так как `<li>` узел был добавлен в список.</span><span class="sxs-lookup"><span data-stu-id="50ce6-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="50ce6-318">Нажмите кнопку **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="50ce6-318">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="50ce6-319">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="50ce6-319">Next steps</span></span>   

<span data-ttu-id="50ce6-320">, Которая охватывает большую часть функций, связанных с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="50ce6-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="50ce6-321">Вы можете найти остальные элементы, щелкнув правой кнопкой мыши узлы в дереве DOM и экспериментируя с другими параметрами, которые не были рассмотрены в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="50ce6-321">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="50ce6-322">Вы также можете просмотреть [сочетания клавиш для панели элементов][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="50ce6-322">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="50ce6-323">Ознакомьтесь с [домашней страницей Microsoft Edge DevTools][MicrosoftEdgeDevTools] , чтобы найти все, что вы можете делать с DevTools.</span><span class="sxs-lookup"><span data-stu-id="50ce6-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="50ce6-324">Приложение: HTML и модель DOM</span><span class="sxs-lookup"><span data-stu-id="50ce6-324">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="50ce6-325">В следующем разделе показано, как быстро рассказано о различиях между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="50ce6-326">При использовании веб-браузера для запроса страницы сервер возвращает HTML-код, как в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="50ce6-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
      <span data-ttu-id="50ce6-327">Браузер анализирует HTML и создает дерево объектов, как в приведенном ниже списке.</span><span class="sxs-lookup"><span data-stu-id="50ce6-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
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

<span data-ttu-id="50ce6-328">Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="50ce6-329">Теперь оно выглядит так же, как HTML, но предположим, что сценарий, указанный в нижней части HTML, выполняет следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="50ce6-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="50ce6-330">Этот код удаляет `h1` узел и добавляет еще один `p` узел в модель DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="50ce6-331">Теперь в качестве полного DOM появится следующий список.</span><span class="sxs-lookup"><span data-stu-id="50ce6-331">The complete DOM now displays the following list.</span></span>  
      
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

<span data-ttu-id="50ce6-332">HTML-код страницы теперь отличается от модели DOM.</span><span class="sxs-lookup"><span data-stu-id="50ce6-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="50ce6-333">Другими словами, HTML представляет начальное содержимое страницы, а модель DOM — текущее содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="50ce6-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="50ce6-334">Когда JavaScript добавляет, удаляет или редактирует узлы, модель DOM становится отличной от HTML.</span><span class="sxs-lookup"><span data-stu-id="50ce6-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="50ce6-335">Дополнительные сведения можно найти в разделе [Введение в модель DOM][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="50ce6-335">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

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

## <span data-ttu-id="50ce6-336">Приложение: отсутствующие параметры</span><span class="sxs-lookup"><span data-stu-id="50ce6-336">Appendix: Missing options</span></span>   

<span data-ttu-id="50ce6-337">Многие инструкции, описанные в этом руководстве, помогут вам щелкнуть правой кнопкой мыши узел в дереве DOM и выбрать нужный вариант в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="50ce6-337">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="50ce6-338">Если указанный параметр не отображается в контекстном меню, попробуйте щелкнуть правой кнопкой мыши за пределами текста узла.</span><span class="sxs-lookup"><span data-stu-id="50ce6-338">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Выбор варианта, если вы не видите все параметры" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="50ce6-340">Выбор варианта, если вы не видите все параметры</span><span class="sxs-lookup"><span data-stu-id="50ce6-340">Where to click if you are not seeing all the options</span></span>  
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
> <span data-ttu-id="50ce6-346">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50ce6-346">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="50ce6-347">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/dom/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="50ce6-347">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="50ce6-349">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50ce6-349">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

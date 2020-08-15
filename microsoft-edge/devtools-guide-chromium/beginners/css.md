---
title: 'DevTools для начинающих: Приступая к работе с CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 6e005f4107764a13934f0c8f3b3cde0ab9bf98c2
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931776"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="b15d5-103">DevTools для начинающих: Приступая к работе с CSS</span><span class="sxs-lookup"><span data-stu-id="b15d5-103">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="b15d5-104">В этом учебнике вы узнаете, как использовать CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="b15d5-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="b15d5-105">Кроме того, вы узнаете, как использовать Microsoft Edge DevTools для экспериментов с изменениями CSS.</span><span class="sxs-lookup"><span data-stu-id="b15d5-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="b15d5-106">В следующей статье приведен второй учебник из серии руководств, в которых рассматриваются основы разработки веб-приложений и Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b15d5-106">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="b15d5-107">Вы получаете практический опыт, завершив создание собственного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="b15d5-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="b15d5-108">Перед вторым учебником вам не нужно выполнять первый из них.</span><span class="sxs-lookup"><span data-stu-id="b15d5-108">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="b15d5-109">[Настройка кода](#set-up-your-code) показывает, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="b15d5-109">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="b15d5-110">Этот учебник предназначен для абсолютных новичков и специализируется на **основах разработки веб-приложений** и основах использования DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="b15d5-110">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="b15d5-111">Если вам нужен учебник, который фокусируется только на DevTools, ознакомьтесь [со статьей Приступая к просмотру и изменению CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="b15d5-111">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="b15d5-112">В начале учебника ваш сайт должен выглядеть так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b15d5-112">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="b15d5-114">Как выглядит ваш веб-сайт</span><span class="sxs-lookup"><span data-stu-id="b15d5-114">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="b15d5-115">После того как вы закончите обучение, сайт должен выглядеть так, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="b15d5-115">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Сведения о том, как должен выглядеть сайт в конце учебника" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="b15d5-117">Сведения о том, как должен выглядеть сайт в конце учебника</span><span class="sxs-lookup"><span data-stu-id="b15d5-117">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <span data-ttu-id="b15d5-118">Цели</span><span class="sxs-lookup"><span data-stu-id="b15d5-118">Goals</span></span>  

<span data-ttu-id="b15d5-119">Следуйте этим рекомендациям, чтобы лучше разобраться в описанных ниже концепциях и задачах.</span><span class="sxs-lookup"><span data-stu-id="b15d5-119">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="b15d5-120">Использование CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="b15d5-120">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="b15d5-121">Использование Microsoft Edge DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="b15d5-121">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="b15d5-122">Разница между платформами CSS и CSS.</span><span class="sxs-lookup"><span data-stu-id="b15d5-122">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="b15d5-123">Вы собираетесь создать реальный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="b15d5-123">You are building a real website.</span></span>  

## <span data-ttu-id="b15d5-124">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="b15d5-124">Prerequisites</span></span>  

<span data-ttu-id="b15d5-125">Перед началом работы с учебником заполните следующие предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="b15d5-125">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="b15d5-126">Закончите [работу с HTML и моделью DOM][DevtoolsBeginnersHtml] или убедитесь в том, что вы знаете HTML и модель DOM, похожую на то, что научились в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="b15d5-126">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="b15d5-127">Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="b15d5-127">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="b15d5-128">В следующем учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b15d5-128">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="b15d5-129">Настройка кода</span><span class="sxs-lookup"><span data-stu-id="b15d5-129">Set up your code</span></span>  

<span data-ttu-id="b15d5-130">Чтобы создать сайт, необходимо выполнить описанные ниже действия, чтобы настроить код.</span><span class="sxs-lookup"><span data-stu-id="b15d5-130">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="b15d5-131">Если вы уже завершили первый учебник в ряду, перейдите к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="b15d5-131">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="b15d5-132">Продолжайте использовать код из последнего учебника, Приступая к [работе с HTML и DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="b15d5-132">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="b15d5-133">Откройте [Исходный код][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="b15d5-133">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="b15d5-134">Ссылка на вкладку "на фокус" в браузере указана как **вкладка "Редактирование"**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-134">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Вкладка "Редактирование"" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="b15d5-136">Вкладка " **Редактирование** "</span><span class="sxs-lookup"><span data-stu-id="b15d5-136">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-137">Выберите **готовил-amphibian**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-137">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="b15d5-138">Всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="b15d5-138">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Меню "Параметры проекта"" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="b15d5-140">Меню "Параметры проекта"</span><span class="sxs-lookup"><span data-stu-id="b15d5-140">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="b15d5-141">Выберите **Remix проект**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-141">Choose **Remix Project**.</span></span>  <span data-ttu-id="b15d5-142">Сбой создает копию проекта, которую вы можете редактировать.</span><span class="sxs-lookup"><span data-stu-id="b15d5-142">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b15d5-143">Сбой генерирует случайное имя для нового проекта.</span><span class="sxs-lookup"><span data-stu-id="b15d5-143">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="b15d5-144">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-144">Choose **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="b15d5-145">Откроется другая вкладка с активным представлением сайта.</span><span class="sxs-lookup"><span data-stu-id="b15d5-145">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="b15d5-146">На вкладку, которая находится в фокусе браузера, указывается **вкладка Динамический**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-146">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Вкладка "динамический"" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="b15d5-148">**Вкладка "динамический"**</span><span class="sxs-lookup"><span data-stu-id="b15d5-148">The **live tab**</span></span>  
    :::image-end:::  

## <span data-ttu-id="b15d5-149">Общие сведения о CSS</span><span class="sxs-lookup"><span data-stu-id="b15d5-149">Understand CSS</span></span>  

<span data-ttu-id="b15d5-150">**CSS** — это язык компьютера, который определяет макет и стиль веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="b15d5-150">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="b15d5-151">На приведенном ниже рисунке показан абзац с границей.</span><span class="sxs-lookup"><span data-stu-id="b15d5-151">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Текст был добавлен в таблицу каскадных стилей (CSS)" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="b15d5-153">Текст был добавлен в таблицу каскадных стилей (CSS)</span><span class="sxs-lookup"><span data-stu-id="b15d5-153">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="b15d5-154">Следующий фрагмент кода — это код HTML и CSS, который используется для создания абзаца на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b15d5-154">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="b15d5-155">возможно, вам покажется, что у вас новый.</span><span class="sxs-lookup"><span data-stu-id="b15d5-155">probably looks new to you.</span></span>  <span data-ttu-id="b15d5-156">Остальные должны выглядеть знакомым.</span><span class="sxs-lookup"><span data-stu-id="b15d5-156">The rest should look familiar.</span></span>  <span data-ttu-id="b15d5-157">Если это не так, сначала приступайте [к работе с HTML и моделью DOM,][DevtoolsBeginnersHtml] прежде чем выполнять следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="b15d5-157">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <span data-ttu-id="b15d5-158">Добавление встроенных стилей</span><span class="sxs-lookup"><span data-stu-id="b15d5-158">Add inline styles</span></span>  

<span data-ttu-id="b15d5-159">Выполните указанные ниже действия, чтобы применить стили к одному элементу с помощью **встроенных стилей** .</span><span class="sxs-lookup"><span data-stu-id="b15d5-159">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="b15d5-160">Вернитесь на вкладку Правка и откройте окно `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-160">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="b15d5-162">Открытие `index.html` на вкладке "Редактирование"</span><span class="sxs-lookup"><span data-stu-id="b15d5-162">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-163">Добавить `style="background-color: aliceblue;"` в `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-163">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="b15d5-164">В блоке кода, приведенном ниже, четвертая строка кода имеет тот же адрес, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="b15d5-164">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="b15d5-165">Остальное – это просто, так что вы можете сделать так, чтобы новый код замещается в нужном расположении.</span><span class="sxs-lookup"><span data-stu-id="b15d5-165">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  <span data-ttu-id="b15d5-166">Перейдите на **вкладку динамический** , чтобы увидеть изменения.</span><span class="sxs-lookup"><span data-stu-id="b15d5-166">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="b15d5-167">`<nav>`Теперь фон раздела синего цвета.</span><span class="sxs-lookup"><span data-stu-id="b15d5-167">The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Цвет фона, который находится за домашней страницей и ссылками на контакты, стал синей" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="b15d5-169">Цвет фона, который находится за **домашней страницей** и ссылками на **Контакты** , стал синей</span><span class="sxs-lookup"><span data-stu-id="b15d5-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b15d5-170">Повторное использование стилей на одной странице с внутренними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="b15d5-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="b15d5-171">В предыдущем фрагменте кода встроенный стиль применяет стиль для одного `<p>` тега.</span><span class="sxs-lookup"><span data-stu-id="b15d5-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="b15d5-172">Что делать, если вы хотите `<p>` , чтобы все элементы на веб-странице были применены таким же образом?</span><span class="sxs-lookup"><span data-stu-id="b15d5-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="b15d5-173">Код необходимо скопировать и вставить в каждый один `<p>` тег на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="b15d5-173">You would have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="b15d5-174">Это немало времени и сил.</span><span class="sxs-lookup"><span data-stu-id="b15d5-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="b15d5-175">Если вы хотите внести изменения, вам придется заново изменить все теги.</span><span class="sxs-lookup"><span data-stu-id="b15d5-175">And, if you needed to make an edit, you would have to change every tag again.</span></span>  <span data-ttu-id="b15d5-176">Выполните указанные ниже действия, чтобы использовать **внутреннюю таблицу стилей** для создания CSS, чтобы она применялась к нескольким элементам.</span><span class="sxs-lookup"><span data-stu-id="b15d5-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="b15d5-177">На вкладке "динамический" нажмите " **контакт** ", чтобы перейти на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="b15d5-177">In the live tab, choose **Contact** to go to the contact page.</span></span>  <span data-ttu-id="b15d5-178">Обратите внимание на шрифт **домашних** и **контактных**данных.</span><span class="sxs-lookup"><span data-stu-id="b15d5-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Страница "контакт"" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="b15d5-180">Страница "контакт"</span><span class="sxs-lookup"><span data-stu-id="b15d5-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-181">На **вкладке "редактор**" перейдите в раздел `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-181">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="b15d5-182">Добавьте следующий код `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="b15d5-183">Помните, что вам нужно добавить строки, начинающиеся с `<style>` и заканчивая данными `</style>` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="b15d5-184">Другой код — это только то, что вы знаете, где разместить новый код.</span><span class="sxs-lookup"><span data-stu-id="b15d5-184">The other code is just there so you know where to put the new code.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  <span data-ttu-id="b15d5-185">Вернитесь на **вкладку динамический**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="b15d5-186">Нажмите кнопку " **контакт** ", чтобы вернуться на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="b15d5-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="b15d5-187">Изменился шрифт " **Главная** " и " **контакт** ".</span><span class="sxs-lookup"><span data-stu-id="b15d5-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Изменен шрифт ссылок на домашнюю страницу и контакт контакта" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="b15d5-189">Изменен шрифт ссылок на **домашнюю страницу** и **контакт контакта**</span><span class="sxs-lookup"><span data-stu-id="b15d5-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b15d5-190">Общие сведения о внутренних таблицах стилей</span><span class="sxs-lookup"><span data-stu-id="b15d5-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="b15d5-191">Внутренние таблицы стилей. Примените стили с помощью **селекторов**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="b15d5-192">Селекторы — это шаблоны, которые могут применяться к одному или нескольким элементам HTML.</span><span class="sxs-lookup"><span data-stu-id="b15d5-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="b15d5-193">Предыдущий фрагмент кода добавил следующий стиль.</span><span class="sxs-lookup"><span data-stu-id="b15d5-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="b15d5-194">— Это селектор, который преобразуется в "любой `<li>` элемент, содержащий `<a>` элемент".</span><span class="sxs-lookup"><span data-stu-id="b15d5-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="b15d5-195">Браузер изменит шрифт **домашних** и **контактных** ссылок, так как каждая из групп тегов соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b15d5-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="b15d5-196">является **объявлением**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-196">is a **declaration**.</span></span>  <span data-ttu-id="b15d5-197">Объявление состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="b15d5-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="b15d5-198">Property</span><span class="sxs-lookup"><span data-stu-id="b15d5-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b15d5-199">Это свойство описывает общий способ изменения стиля элемента.</span><span class="sxs-lookup"><span data-stu-id="b15d5-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="b15d5-200">value</span><span class="sxs-lookup"><span data-stu-id="b15d5-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b15d5-201">Значение точно описывает способ изменения стиля элемента.</span><span class="sxs-lookup"><span data-stu-id="b15d5-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="b15d5-202">Например, `font-family: 'Courier New', Courier, serif` предоставляет браузеру следующую инструкцию: "Установка шрифта для элементов, которые соответствуют шаблону `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="b15d5-203">Если этот шрифт недоступен, используйте `Courier` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="b15d5-204">Если это недоступно, используйте `serif` ".</span><span class="sxs-lookup"><span data-stu-id="b15d5-204">If that is not available, use `serif`."</span></span>  

### <span data-ttu-id="b15d5-205">Добавление нескольких селекторов в набор правил</span><span class="sxs-lookup"><span data-stu-id="b15d5-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="b15d5-206">Блок кода CSS вроде того, что вы видите ниже, называется набором **правил**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-206">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="b15d5-207">Выполните следующие действия, чтобы добавить несколько селекторов в RuleSet с помощью запятых.</span><span class="sxs-lookup"><span data-stu-id="b15d5-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="b15d5-208">На **вкладке Редактор**откройте `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="b15d5-209">После `li a` ввода `, h1` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="b15d5-210">Предыдущий фрагмент кода указывает браузеру на элементы стиля `<h1>` таким же образом, как и элементы, которые соответствуют шаблону `li a` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="b15d5-211">Перейдите на **вкладку динамический**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-211">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="b15d5-212">Щелкните ссылку **контакт** , чтобы вернуться на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="b15d5-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="b15d5-213">Теперь **свяжитесь со мной!**</span><span class="sxs-lookup"><span data-stu-id="b15d5-213">Now, **Contact Me!**</span></span> <span data-ttu-id="b15d5-214">имеет тот же шрифт, что и ссылки для навигации.</span><span class="sxs-lookup"><span data-stu-id="b15d5-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Текстовые контакты!  Теперь тот же шрифт, что и ссылки на домашнюю и контактный" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="b15d5-217">Текстовые **Контакты!**</span><span class="sxs-lookup"><span data-stu-id="b15d5-217">The text **Contact Me!**</span></span> <span data-ttu-id="b15d5-218">Теперь тот же шрифт, что и ссылки на **домашнюю** и **контактный**</span><span class="sxs-lookup"><span data-stu-id="b15d5-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b15d5-219">Поэкспериментировать с DevTools</span><span class="sxs-lookup"><span data-stu-id="b15d5-219">Experiment with DevTools</span></span>  

<span data-ttu-id="b15d5-220">По мере того как вы продолжите свое путешествие, чтобы стать экспертом при разработке веб-приложений, возможно, вы обнаружите, что CSS очень сложны.</span><span class="sxs-lookup"><span data-stu-id="b15d5-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="b15d5-221">Вы можете написать каскадную таблицу стилей, чтобы она отображалась одним способом, но браузер делает что-то совершенно другое.</span><span class="sxs-lookup"><span data-stu-id="b15d5-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="b15d5-222">Microsoft Edge DevTools упрощает эксперименты с изменениями и немедленно показывает, как изменения повлияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="b15d5-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how the changes affect the page.</span></span>  

### <span data-ttu-id="b15d5-223">Добавление объявления к существующему правилу в DevTools</span><span class="sxs-lookup"><span data-stu-id="b15d5-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="b15d5-224">Выполните указанные ниже действия, чтобы выполнить итерацию по стилю существующего элемента, добавив объявление к существующему набору правил.</span><span class="sxs-lookup"><span data-stu-id="b15d5-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="b15d5-225">Наведите указатель мыши на **домашнюю** ссылку, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-225">Hover on the **Home** link, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Проверка ссылки на домашнюю страницу" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="b15d5-227">Проверка ссылки на домашнюю страницу</span><span class="sxs-lookup"><span data-stu-id="b15d5-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="b15d5-228">DevTools открывается вместе со страницей.</span><span class="sxs-lookup"><span data-stu-id="b15d5-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="b15d5-229">Код, представляющий ссылку на домашнюю страницу, `<a href="/">Home</a>` выделяется синим цветом в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="b15d5-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="b15d5-230">Фрагмент кода и предварительный просмотр должны быть знакомы с тем, как начать [работу с HTML и моделью DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="b15d5-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="b15d5-231">На приведенном ниже рисунке `font-family: 'Courier New', Courier, serif` объявление, добавленное ранее, отображается `contact.html` на вкладке **стили** под деревом DOM.</span><span class="sxs-lookup"><span data-stu-id="b15d5-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is seen in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Вкладка "стили" находится под деревом DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="b15d5-233">Вкладка " **стили** " находится под ДЕРЕВОм DOM</span><span class="sxs-lookup"><span data-stu-id="b15d5-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="b15d5-234">Если окно DevTools является широкой страницей, вкладка стили находится справа от дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="b15d5-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Вкладка "стили" справа от дерева DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="b15d5-236">Вкладка " **стили** " справа от дерева DOM</span><span class="sxs-lookup"><span data-stu-id="b15d5-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="b15d5-237">Чтобы добавить новое объявление, выберите пустую строку ниже `font-family: 'Courier New', Courier, Serif` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Добавление нового объявления" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="b15d5-239">Добавление нового объявления</span><span class="sxs-lookup"><span data-stu-id="b15d5-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-240">Введите текст `color` и выберите его `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="b15d5-241">Пользовательский интерфейс автозаполнения предлагает параметры по мере ввода.</span><span class="sxs-lookup"><span data-stu-id="b15d5-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Введите цвет" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="b15d5-243">Тип</span><span class="sxs-lookup"><span data-stu-id="b15d5-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-244">Введите текст `magenta` и выберите его `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="b15d5-245">Весь текст на странице контакта стал пурпурным.</span><span class="sxs-lookup"><span data-stu-id="b15d5-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Введите пурпурный" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="b15d5-247">Тип</span><span class="sxs-lookup"><span data-stu-id="b15d5-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <span data-ttu-id="b15d5-248">Изменение объявления в DevTools</span><span class="sxs-lookup"><span data-stu-id="b15d5-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="b15d5-249">Чтобы изменить существующие объявления в DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b15d5-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="b15d5-250">Выберите пурпурный квадрат рядом с `magenta` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="b15d5-251">Появится палитра выбора цвета.</span><span class="sxs-lookup"><span data-stu-id="b15d5-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Выбор цвета" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="b15d5-253">Выбор цвета</span><span class="sxs-lookup"><span data-stu-id="b15d5-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-254">С помощью средства выбора цвета измените текст шрифта на нужный цвет.</span><span class="sxs-lookup"><span data-stu-id="b15d5-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="b15d5-256">Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="b15d5-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b15d5-257">Добавление нового набора правил в DevTools</span><span class="sxs-lookup"><span data-stu-id="b15d5-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="b15d5-258">Чтобы добавить новые наборы правил в DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b15d5-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="b15d5-259">Выберите **новое правило стиля** \ ( ![ новое правило стиля ][ImageNewStyleRuleIcon] \), которое находится рядом с **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="b15d5-260">В качестве Selector появится пустой набор правил `a` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Добавление нового правила" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="b15d5-262">Добавление нового правила</span><span class="sxs-lookup"><span data-stu-id="b15d5-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-263">Заменить `a` на `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Замена a на a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="b15d5-265">Заменить `a` на</span><span class="sxs-lookup"><span data-stu-id="b15d5-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="b15d5-266">является **псевдо-классом**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="b15d5-267">Используйте псевдо-классы для элементов стиля, которые могут вводить особые состояния.</span><span class="sxs-lookup"><span data-stu-id="b15d5-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="b15d5-268">Например, `a:hover` стиль вступает в силу только при наведении указателя мыши на `<a>` элемент.</span><span class="sxs-lookup"><span data-stu-id="b15d5-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="b15d5-269">Выберите между скобками, чтобы добавить новое объявление.</span><span class="sxs-lookup"><span data-stu-id="b15d5-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="b15d5-270">Введите `background-color` имя объявления и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Введите цвет фона" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="b15d5-272">Тип</span><span class="sxs-lookup"><span data-stu-id="b15d5-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-273">Введите `green` значение объявления и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Введите зеленый цвет" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="b15d5-275">Тип</span><span class="sxs-lookup"><span data-stu-id="b15d5-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-276">Наведите указатель мыши на ссылку " **Домашняя страница** ".</span><span class="sxs-lookup"><span data-stu-id="b15d5-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="b15d5-277">Фон ссылки становится зеленым.</span><span class="sxs-lookup"><span data-stu-id="b15d5-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="b15d5-279">Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон</span><span class="sxs-lookup"><span data-stu-id="b15d5-279">Hover over the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b15d5-280">Повторное использование стилей на разных страницах с внешними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="b15d5-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="b15d5-281">На предыдущем этапе вы добавили следующий фрагмент кода в качестве внутренней таблицы стилей `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

<span data-ttu-id="b15d5-282">Что делать, если вы захотите стиль `index.html` одинаково?</span><span class="sxs-lookup"><span data-stu-id="b15d5-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="b15d5-283">Что делать, если вы хотите применить стили к большому количеству страниц?</span><span class="sxs-lookup"><span data-stu-id="b15d5-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="b15d5-284">Необходимо скопировать и вставить внутреннюю таблицу стилей в каждую веб-страницу на сайте.</span><span class="sxs-lookup"><span data-stu-id="b15d5-284">You would have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="b15d5-285">Выполните указанные ниже действия, чтобы добавить **внешнюю таблицу стилей** , которая позволит вам создавать CSS один раз и применять ее к нескольким страницам.</span><span class="sxs-lookup"><span data-stu-id="b15d5-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="b15d5-286">Сначала перезагрузите вкладку Live, чтобы удалить изменения, внесенные в DevTools.</span><span class="sxs-lookup"><span data-stu-id="b15d5-286">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" После обновления страницы изменения, внесенные в DevTools, исчезают" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="b15d5-288">После обновления страницы изменения, внесенные в DevTools, исчезают</span><span class="sxs-lookup"><span data-stu-id="b15d5-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-289">Вернитесь на **вкладку Редактор** и откройте ее `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="b15d5-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="b15d5-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-292">Удалить все между `<style>` и `</style>` , включая `<style>` и `</style>` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Тег Style был удален" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="b15d5-294">Тег Style был удален</span><span class="sxs-lookup"><span data-stu-id="b15d5-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-295">Перейдите к `index.html` тегу и удалите `style="background-color: aliceblue;"` его `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-295">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="b15d5-296">Теперь вы удалили все CSS-таблицы, которые вы ранее добавили на сайт.</span><span class="sxs-lookup"><span data-stu-id="b15d5-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Встроенный стиль удален из элемента навигации" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="b15d5-298">Встроенный стиль удален из элемента навигации</span><span class="sxs-lookup"><span data-stu-id="b15d5-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-299">Выберите команду **создать файл**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Диалоговое окно "Создание файла"" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="b15d5-301">Диалоговое окно "Создание файла"</span><span class="sxs-lookup"><span data-stu-id="b15d5-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-302">Замените `cool-file.js` на `style.css` и выберите команду **Добавить файл**.</span><span class="sxs-lookup"><span data-stu-id="b15d5-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Введите Style. CSS" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="b15d5-304">Тип</span><span class="sxs-lookup"><span data-stu-id="b15d5-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-305">Добавьте в файл следующий фрагмент кода `style.css` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-305">Add the following code snippet to your `style.css` file.</span></span>  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Добавление кода в Style. CSS" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="b15d5-307">Добавление кода в</span><span class="sxs-lookup"><span data-stu-id="b15d5-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="b15d5-308">Убедитесь, что создана внешняя таблица стилей.</span><span class="sxs-lookup"><span data-stu-id="b15d5-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="b15d5-309">Ваш HTML-код не знает, что он существует.</span><span class="sxs-lookup"><span data-stu-id="b15d5-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="b15d5-310">Open (открыть) `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="b15d5-311">Добавьте `<link rel="stylesheet" href="style.css">` в свой HTML-код.</span><span class="sxs-lookup"><span data-stu-id="b15d5-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Ссылка на стиль Style. CSS" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="b15d5-313">Ссылка на</span><span class="sxs-lookup"><span data-stu-id="b15d5-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-314">Откройте `contact.html` файл и добавьте ссылку на него.</span><span class="sxs-lookup"><span data-stu-id="b15d5-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Ссылка на стиль Style. CSS в contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="b15d5-316">Ссылка `style.css` в</span><span class="sxs-lookup"><span data-stu-id="b15d5-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-317">Перейдите на **вкладку динамический**.  Домашняя страница теперь имеет тот же шрифт, что и в последнем разделе, и в синем разделе навигации.</span><span class="sxs-lookup"><span data-stu-id="b15d5-317">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Домашняя страница" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="b15d5-319">Домашняя страница</span><span class="sxs-lookup"><span data-stu-id="b15d5-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-320">Щелкните ссылку **контакт** , чтобы перейти на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="b15d5-320">Choose the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="b15d5-321">Страница контакта имеет тот же формат, что и домашняя страница.</span><span class="sxs-lookup"><span data-stu-id="b15d5-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Страница "контакт"" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="b15d5-323">Страница "контакт"</span><span class="sxs-lookup"><span data-stu-id="b15d5-323">The contact page</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b15d5-324">Использование платформы CSS</span><span class="sxs-lookup"><span data-stu-id="b15d5-324">Use a CSS framework</span></span>  

<span data-ttu-id="b15d5-325">**Платформы CSS** — это коллекции стилей, разработанных другими разработчиками, которые упрощают создание привлекательных веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="b15d5-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="b15d5-326">Вместо того чтобы определять стили самостоятельно, платформа предоставляет коллекцию стилей, которые вы можете использовать в элементах страницы.</span><span class="sxs-lookup"><span data-stu-id="b15d5-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="b15d5-327">Скопируйте приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="b15d5-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="b15d5-328">Перейдите на вкладку Правка и вставьте код в `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-328">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Ссылка на платформу в contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="b15d5-330">Ссылка на платформу в</span><span class="sxs-lookup"><span data-stu-id="b15d5-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-331">Откройте `index.html` файл и добавьте в него код.</span><span class="sxs-lookup"><span data-stu-id="b15d5-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Ссылка на платформу в index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="b15d5-333">Ссылка на платформу в</span><span class="sxs-lookup"><span data-stu-id="b15d5-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-334">Вернитесь на вкладку динамический, чтобы просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="b15d5-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="b15d5-335">Несмотря на то, что цвет фона `<nav>` элемента и шрифта `<li>` `<a>` элементов and одинаков, изменился шрифт остальных элементов.</span><span class="sxs-lookup"><span data-stu-id="b15d5-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Некоторые шрифты на домашней странице изменились из-за платформы" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="b15d5-337">Некоторые шрифты на домашней странице изменились из-за платформы</span><span class="sxs-lookup"><span data-stu-id="b15d5-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b15d5-338">Использование класса</span><span class="sxs-lookup"><span data-stu-id="b15d5-338">Use a class</span></span>  

<span data-ttu-id="b15d5-339">В последнем разделе вы добавили начальную загрузку на веб-страницы, которая изменила шрифты для некоторых элементов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="b15d5-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="b15d5-340">Структуры CSS помогают вносить существенные изменения на странице с помощью очень небольшого количества кода.</span><span class="sxs-lookup"><span data-stu-id="b15d5-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="b15d5-341">Чтобы изменить верхний колонтитул, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b15d5-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="b15d5-342">Скопируйте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="b15d5-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="b15d5-343">Добавьте предыдущий фрагмент кода в `<header>` тег `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Добавление классов в index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="b15d5-345">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="b15d5-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-346">Добавьте код в `<header>` тег `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Добавление классов в contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="b15d5-348">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="b15d5-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-349">Просмотрите изменения на вкладке "живые".  Вокруг заголовка есть большое затененное поле.</span><span class="sxs-lookup"><span data-stu-id="b15d5-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него." lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="b15d5-351">Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него.</span><span class="sxs-lookup"><span data-stu-id="b15d5-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b15d5-352">Общие сведения о классах</span><span class="sxs-lookup"><span data-stu-id="b15d5-352">Understand classes</span></span>  

<span data-ttu-id="b15d5-353">Классы позволяют назначать коллекции стилей произвольным элементам.</span><span class="sxs-lookup"><span data-stu-id="b15d5-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="b15d5-354">Используйте следующий фрагмент кода, чтобы применить к `<header>` элементу несколько стилей после присвоения `class` атрибуту значения `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="b15d5-355">Одно из преимуществ класса состоит в том, что он позволяет применять стили к любым нужным элементам.</span><span class="sxs-lookup"><span data-stu-id="b15d5-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="b15d5-356">Например, предположим, что вам нужно установить для некоторых элементов цвет фона `<p>` , который будет фиолетовым, но не все `<p>` элементы.</span><span class="sxs-lookup"><span data-stu-id="b15d5-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="b15d5-357">Используйте следующий фрагмент кода, чтобы определить стиль в классе.</span><span class="sxs-lookup"><span data-stu-id="b15d5-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="b15d5-358">Затем примените класс только к тем `<p>` элементам, для которых вы хотите применить стиль.</span><span class="sxs-lookup"><span data-stu-id="b15d5-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <span data-ttu-id="b15d5-359">Выравнивание элементов</span><span class="sxs-lookup"><span data-stu-id="b15d5-359">Align elements</span></span>  

<span data-ttu-id="b15d5-360">Выполните указанные ниже действия, чтобы выполнить загрузку и предоставить классы для выравнивания элементов.</span><span class="sxs-lookup"><span data-stu-id="b15d5-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="b15d5-361">Вернитесь на вкладку Редактор и откройте ее `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="b15d5-362">Добавьте `class="container-fluid"` в свой `<body>` тег.</span><span class="sxs-lookup"><span data-stu-id="b15d5-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Добавление класса Container-жидкости" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="b15d5-364">Добавьте `container-fluid` класс</span><span class="sxs-lookup"><span data-stu-id="b15d5-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-365">Обтекание `<nav>` `<main>` элементов `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="b15d5-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="b15d5-366">`</div>`Чтобы правильно закрыть новый тег, убедитесь в том, что вы хотите сделать `</main>` это.</span><span class="sxs-lookup"><span data-stu-id="b15d5-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Добавление строки" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="b15d5-368">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="b15d5-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-369">Добавьте `class="col-3"` теги в тег `<nav>` и `class="col-9"` в `<main>` тег.</span><span class="sxs-lookup"><span data-stu-id="b15d5-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Добавление классов Col-3 и Col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="b15d5-371">Добавление `col-3` классов и `col-9`</span><span class="sxs-lookup"><span data-stu-id="b15d5-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b15d5-372">Просмотрите изменения на вкладке "живые".</span><span class="sxs-lookup"><span data-stu-id="b15d5-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Содержимое элемента навигации теперь находится слева от основного содержимого." lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="b15d5-374">Содержимое элемента навигации теперь находится слева от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="b15d5-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b15d5-375">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="b15d5-375">Next steps</span></span>  

<span data-ttu-id="b15d5-376">Поздравляем, вы закончите.</span><span class="sxs-lookup"><span data-stu-id="b15d5-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="b15d5-377">Лучший способ улучшить качество веб-приложений — создать дополнительные сайты.</span><span class="sxs-lookup"><span data-stu-id="b15d5-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="b15d5-378">Не беспокойтесь о нарушениях.</span><span class="sxs-lookup"><span data-stu-id="b15d5-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="b15d5-379">Просто восприятие и обучение очень удобно.</span><span class="sxs-lookup"><span data-stu-id="b15d5-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="b15d5-380">Чтобы узнать больше о стилях веб-страниц, ознакомьтесь со статьей общие сведения о [CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="b15d5-380">To learn more about styling web pages, see [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="b15d5-381">Дополнительные сведения о том, как использовать DevTools для экспериментов с CSS-страницей, можно найти в статье Начало [работы с помощью просмотра и изменения CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="b15d5-381">To learn more about how to use DevTools to experiment with the CSS of a page, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools для начинающих: Приступая к работе с HTML и моделью DOM | Документы Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-готовил-amphibian | Цепь"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Первые шаги CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="b15d5-387">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b15d5-387">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b15d5-388">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/css) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="b15d5-388">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b15d5-390">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b15d5-390">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  

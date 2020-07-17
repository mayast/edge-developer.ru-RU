---
title: 'DevTools для начинающих: Приступая к работе с CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: fba049a20a7b5f981130b4d9e60c37b07dc7e092
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882739"
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

# <span data-ttu-id="19502-103">DevTools для начинающих: Приступая к работе с CSS</span><span class="sxs-lookup"><span data-stu-id="19502-103">DevTools for beginners: Get started with CSS</span></span>   

<span data-ttu-id="19502-104">В этом учебнике вы узнаете, как использовать CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="19502-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="19502-105">Кроме того, вы узнаете, как использовать Microsoft Edge DevTools для экспериментов с изменениями CSS.</span><span class="sxs-lookup"><span data-stu-id="19502-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="19502-106">Это второй учебник из ряда учебников, в котором рассказывается о том, что такое веб-разработка и Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="19502-106">This is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="19502-107">Вы получаете практический опыт, завершив создание собственного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="19502-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="19502-108">Вам не нужно выполнять первый учебник, прежде чем делать это.</span><span class="sxs-lookup"><span data-stu-id="19502-108">You don't have to complete the first tutorial before doing this one.</span></span>  <span data-ttu-id="19502-109">Здесь вы можете приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="19502-109">You can start here.</span></span>  <span data-ttu-id="19502-110">[Настройка кода](#set-up-your-code) показывает, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="19502-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="19502-111">Этот учебник предназначен для абсолютных новичков и специализируется на **основах разработки веб-приложений** и основах использования DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="19502-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="19502-112">Если вам нужен учебник, который фокусируется только на DevTools, ознакомьтесь [со статьей Приступая к просмотру и изменению CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="19502-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="19502-113">На данный момент ваш веб-сайт выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19502-113">Currently your site looks like this:</span></span>  

> ##### <span data-ttu-id="19502-114">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="19502-114">Figure 1</span></span>  
> <span data-ttu-id="19502-115">Как выглядит ваш веб-сайт</span><span class="sxs-lookup"><span data-stu-id="19502-115">What your site currently looks like</span></span>  
> ![Как выглядит ваш веб-сайт][ImageCssIntro1]  

<span data-ttu-id="19502-117">После завершения работы с учебником он будет выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="19502-117">After completing the tutorial, it will look like this:</span></span>  

> ##### <span data-ttu-id="19502-118">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="19502-118">Figure 2</span></span>  
> <span data-ttu-id="19502-119">Как будет выглядеть ваш веб-сайт в конце учебника</span><span class="sxs-lookup"><span data-stu-id="19502-119">What your site will look like at the end of the tutorial</span></span>  
> ![Как будет выглядеть ваш веб-сайт в конце учебника][ImageCssIntro2]  

## <span data-ttu-id="19502-121">Цели</span><span class="sxs-lookup"><span data-stu-id="19502-121">Goals</span></span>   

<span data-ttu-id="19502-122">В конце этого учебника вы узнаете:</span><span class="sxs-lookup"><span data-stu-id="19502-122">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="19502-123">Использование CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="19502-123">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="19502-124">Использование Microsoft Edge DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="19502-124">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="19502-125">Разница между платформами CSS и CSS.</span><span class="sxs-lookup"><span data-stu-id="19502-125">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="19502-126">У тебя также есть реальный веб-сайт!</span><span class="sxs-lookup"><span data-stu-id="19502-126">You'll also have a real website!</span></span>  

## <span data-ttu-id="19502-127">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="19502-127">Prerequisites</span></span>   

<span data-ttu-id="19502-128">Прежде чем приступить к работе с учебником, выполните следующие требования:</span><span class="sxs-lookup"><span data-stu-id="19502-128">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="19502-129">Закончите [работу с HTML и моделью DOM][DevToolsBeginnersHtml] или убедитесь в том, что вы знаете HTML и модель DOM, похожую на то, что научились в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="19502-129">Complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what's taught in that tutorial.</span></span>  
*   <span data-ttu-id="19502-130">Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="19502-130">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="19502-131">В этом учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="19502-131">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="19502-132">Настройка кода</span><span class="sxs-lookup"><span data-stu-id="19502-132">Set up your code</span></span>   

<span data-ttu-id="19502-133">Чтобы приступить к созданию сайта, вам нужно настроить код:</span><span class="sxs-lookup"><span data-stu-id="19502-133">In order to start creating your site, you need to set up your code:</span></span>  

1.  **<span data-ttu-id="19502-134">Если вы уже завершили первый учебник в этой серии, пропустите этот раздел.</span><span class="sxs-lookup"><span data-stu-id="19502-134">If you have already completed the first tutorial in this series, skip this section!</span></span>  <span data-ttu-id="19502-135">Продолжайте использовать код из последнего учебника, Приступая к [работе с HTML и DOM][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="19502-135">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>**  
1.  <span data-ttu-id="19502-136">Откройте [Исходный код][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="19502-136">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="19502-137">Эта вкладка браузера будет называться **вкладкой "Редактирование"**.</span><span class="sxs-lookup"><span data-stu-id="19502-137">This tab of your browser will be called the **editing tab**.</span></span>  
    
    > ##### <span data-ttu-id="19502-138">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="19502-138">Figure 3</span></span>  
    > <span data-ttu-id="19502-139">Вкладка "Редактирование"</span><span class="sxs-lookup"><span data-stu-id="19502-139">The editing tab</span></span>  
    > ![Вкладка "Редактирование"][ImageCssSetup1]  
    
1.  <span data-ttu-id="19502-141">Щелкните **готовил-amphibian**.</span><span class="sxs-lookup"><span data-stu-id="19502-141">Click **cooked-amphibian**.</span></span>  <span data-ttu-id="19502-142">Всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="19502-142">A menu pops up.</span></span>  
    
    > ##### <span data-ttu-id="19502-143">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="19502-143">Figure 4</span></span>  
    > <span data-ttu-id="19502-144">Меню "Параметры проекта"</span><span class="sxs-lookup"><span data-stu-id="19502-144">The Project Options menu</span></span>  
    > ![Меню "Параметры проекта"][ImageCssSetup2]  

1.  <span data-ttu-id="19502-146">Щелкните **Remix Project (проект**).</span><span class="sxs-lookup"><span data-stu-id="19502-146">Click **Remix Project**.</span></span>  <span data-ttu-id="19502-147">Сбой создает копию проекта, которую можно изменить.</span><span class="sxs-lookup"><span data-stu-id="19502-147">Glitch creates a copy of the project that you can edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="19502-148">Сбой генерирует случайное имя для нового проекта.</span><span class="sxs-lookup"><span data-stu-id="19502-148">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="19502-149">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="19502-149">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="19502-150">Откроется другая вкладка с активным представлением сайта.</span><span class="sxs-lookup"><span data-stu-id="19502-150">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="19502-151">Эта вкладка браузера будет называться **вкладкой Быстрая**.</span><span class="sxs-lookup"><span data-stu-id="19502-151">This tab of your browser will be called the **live tab**.</span></span>  
    
    > ##### <span data-ttu-id="19502-152">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="19502-152">Figure 5</span></span>  
    > <span data-ttu-id="19502-153">Вкладка "динамический"</span><span class="sxs-lookup"><span data-stu-id="19502-153">The live tab</span></span>  
    > ![Вкладка "динамический"][ImageCssSetup3]  

## <span data-ttu-id="19502-155">Общие сведения о CSS</span><span class="sxs-lookup"><span data-stu-id="19502-155">Understand CSS</span></span>   

<span data-ttu-id="19502-156">**CSS** — это язык компьютера, который определяет макет и стиль веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="19502-156">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="19502-157">Например, вот абзац с границей:</span><span class="sxs-lookup"><span data-stu-id="19502-157">For example, here is a paragraph with a border:</span></span>  

> ##### <span data-ttu-id="19502-158">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="19502-158">Figure 6</span></span>  
> <span data-ttu-id="19502-159">Этот стиль помечен с помощью CSS</span><span class="sxs-lookup"><span data-stu-id="19502-159">This has been styled with CSS</span></span>  
> ![Этот стиль помечен с помощью CSS][ImageCssStyled]  

<span data-ttu-id="19502-161">Ниже приведен код HTML и CSS, который используется для создания абзаца.</span><span class="sxs-lookup"><span data-stu-id="19502-161">Here is the HTML and CSS code used to create that paragraph:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="19502-162">возможно, вам покажется, что у вас новый.</span><span class="sxs-lookup"><span data-stu-id="19502-162">probably looks new to you.</span></span>  <span data-ttu-id="19502-163">Остальные должны выглядеть знакомым.</span><span class="sxs-lookup"><span data-stu-id="19502-163">The rest should look familiar.</span></span>  <span data-ttu-id="19502-164">Если это не так, сначала приступайте [к работе с помощью HTML и DOM][DevToolsBeginnersHtml] перед тем, как попытаться воспользоваться этим учебником.</span><span class="sxs-lookup"><span data-stu-id="19502-164">If not, complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] before attempting this tutorial.</span></span>  

## <span data-ttu-id="19502-165">Добавление встроенных стилей</span><span class="sxs-lookup"><span data-stu-id="19502-165">Add inline styles</span></span>   

<span data-ttu-id="19502-166">Используйте **встроенные стили** , если вы хотите применить стили к одному элементу.</span><span class="sxs-lookup"><span data-stu-id="19502-166">Use **inline styles** when you want to apply styles to a single element.</span></span>  <span data-ttu-id="19502-167">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-167">Try it now:</span></span>  

1.  <span data-ttu-id="19502-168">Вернитесь на вкладку Правка и откройте окно `index.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-168">Go back to the editing tab and open `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="19502-169">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="19502-169">Figure 7</span></span>  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  <span data-ttu-id="19502-171">Добавить `style="background-color: aliceblue;"` в `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="19502-171">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="19502-172">В блоке кода, приведенном ниже, четвертая строка кода имеет тот же адрес, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="19502-172">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="19502-173">Вот и все! вы можете сделать так, чтобы в нужном окне вы могли поместить новый код в нужное место.</span><span class="sxs-lookup"><span data-stu-id="19502-173">The rest is just there so you can be sure that you're putting the new code in the right place.</span></span>  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  <span data-ttu-id="19502-174">Перейдите на **вкладку динамический** , чтобы увидеть изменения.</span><span class="sxs-lookup"><span data-stu-id="19502-174">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="19502-175">`<nav>`Теперь фон раздела синего цвета.</span><span class="sxs-lookup"><span data-stu-id="19502-175">The background of the `<nav>` section is now blue.</span></span>  
    
    > ##### <span data-ttu-id="19502-176">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="19502-176">Figure 8</span></span>  
    > <span data-ttu-id="19502-177">Цвет фона, который находится за домашней страницей и ссылками на контакты, стал синей</span><span class="sxs-lookup"><span data-stu-id="19502-177">The background color behind the Home and Contact links is now blue</span></span>  
    > ![Цвет фона, который находится за домашней страницей и ссылками на контакты, стал синей][ImageCssInline2]  

## <span data-ttu-id="19502-179">Повторное использование стилей на одной странице с внутренними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="19502-179">Re-use styles on a single page with internal stylesheets</span></span>   

<span data-ttu-id="19502-180">Ранее вы увидели встроенный стиль, который применяет стиль для одного тега, `<p>` как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="19502-180">Earlier, you saw an inline style that applied a style to a single `<p>` tag like this:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="19502-181">Что делать, если вы хотите `<p>` , чтобы все элементы на веб-странице были применены таким же образом?</span><span class="sxs-lookup"><span data-stu-id="19502-181">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="19502-182">Вам потребуется скопировать код и вставить его в каждый один `<p>` тег на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="19502-182">You'd have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="19502-183">Это не слишком много времени и сил.</span><span class="sxs-lookup"><span data-stu-id="19502-183">That's a lot of time and effort.</span></span>  <span data-ttu-id="19502-184">Если вы хотите внести изменения, вам придется заново изменить каждый из тегов.</span><span class="sxs-lookup"><span data-stu-id="19502-184">And, if you needed to make an edit, you'd have to change every tag again.</span></span>  <span data-ttu-id="19502-185">**Внутренние таблицы стилей** позволяют создавать CSS один раз, чтобы она применялась к нескольким элементам.</span><span class="sxs-lookup"><span data-stu-id="19502-185">**Internal stylesheets** allow you to write your CSS once so that it applies to multiple elements.</span></span>  <span data-ttu-id="19502-186">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-186">Try it now:</span></span>  

1.  <span data-ttu-id="19502-187">На вкладке динамический щелкните **контакт** , чтобы перейти на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="19502-187">In the live tab, click **Contact** to go to the contact page.</span></span>  <span data-ttu-id="19502-188">Обратите внимание на шрифт **домашних** и **контактных**данных.</span><span class="sxs-lookup"><span data-stu-id="19502-188">Notice the font of **Home** and **Contact**.</span></span>  
    
    > ##### <span data-ttu-id="19502-189">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="19502-189">Figure 9</span></span>  
    > <span data-ttu-id="19502-190">Страница "контакт"</span><span class="sxs-lookup"><span data-stu-id="19502-190">The Contact page</span></span>  
    > ![Страница "контакт"][ImageCssInternal1]  

1.  <span data-ttu-id="19502-192">На **вкладке "редактор**" перейдите в раздел `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-192">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="19502-193">Добавьте следующий код `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-193">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="19502-194">Помните, что вам нужно добавить строки, начинающиеся с `<style>` и заканчивая данными `</style>` .</span><span class="sxs-lookup"><span data-stu-id="19502-194">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="19502-195">Другой код — это только то, что вы знаете, где разместить новый код.</span><span class="sxs-lookup"><span data-stu-id="19502-195">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="19502-196">Вернитесь на **вкладку динамический**.</span><span class="sxs-lookup"><span data-stu-id="19502-196">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="19502-197">Нажмите кнопку " **контакт** ", чтобы вернуться на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="19502-197">Click **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="19502-198">Изменился шрифт " **Главная** " и " **контакт** ".</span><span class="sxs-lookup"><span data-stu-id="19502-198">The font of **Home** and **Contact** has changed.</span></span>  
    
    > ##### <span data-ttu-id="19502-199">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="19502-199">Figure 10</span></span>  
    > <span data-ttu-id="19502-200">Изменен шрифт ссылок на домашнюю страницу и контакт контакта</span><span class="sxs-lookup"><span data-stu-id="19502-200">The font of the Home and Contact links has changed</span></span>  
    > ![Изменен шрифт ссылок на домашнюю страницу и контакт контакта][ImageCssInternal2]  
    
### <span data-ttu-id="19502-202">Общие сведения о внутренних таблицах стилей</span><span class="sxs-lookup"><span data-stu-id="19502-202">Understand internal stylesheets</span></span>   

<span data-ttu-id="19502-203">Внутренние таблицы стилей. Примените стили с помощью **селекторов**.</span><span class="sxs-lookup"><span data-stu-id="19502-203">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="19502-204">Селекторы — это шаблоны, которые могут применяться к одному или нескольким элементам HTML.</span><span class="sxs-lookup"><span data-stu-id="19502-204">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="19502-205">Например, в предыдущем коде выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19502-205">For example, in the previous code:</span></span>  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` <span data-ttu-id="19502-206">— Это селектор, который преобразуется в "Any `<li>` , которая содержит `<a>` ".</span><span class="sxs-lookup"><span data-stu-id="19502-206">is a selector that translates to "any `<li>` that contains an `<a>`".</span></span>  <span data-ttu-id="19502-207">Браузер изменит шрифт **домашних** и **контактных** ссылок, так как они соответствуют этому шаблону.</span><span class="sxs-lookup"><span data-stu-id="19502-207">The browser changes the font of the **Home** and **Contact** links because they match this pattern.</span></span>  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="19502-208">является **объявлением**.</span><span class="sxs-lookup"><span data-stu-id="19502-208">is a **declaration**.</span></span>  <span data-ttu-id="19502-209">Объявление состоит из двух частей: **Свойства** и **значения**.</span><span class="sxs-lookup"><span data-stu-id="19502-209">A declaration is made of two parts: a **property** and a **value**.</span></span>  `font-family` <span data-ttu-id="19502-210">является свойством и `'Courier New', Courier, serif` является значением этого свойства.</span><span class="sxs-lookup"><span data-stu-id="19502-210">is the property, and `'Courier New', Courier, serif` is the value of that property.</span></span>  <span data-ttu-id="19502-211">Свойство описывает общий способ изменения стиля элемента, а также указывает, как именно оно должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="19502-211">The property describes a general way that you can change the element's style, and the value says how exactly it should change.</span></span>  <span data-ttu-id="19502-212">Например, `font-family: 'Courier New', Courier, serif` предоставляет браузеру следующую инструкцию: "Установка шрифта элементов, которые соответствуют шаблону `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="19502-212">For example, `font-family: 'Courier New', Courier, serif` gives the browser this instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="19502-213">Если этот шрифт недоступен, используйте `Courier` .</span><span class="sxs-lookup"><span data-stu-id="19502-213">If that font isn't available, use `Courier`.</span></span>  <span data-ttu-id="19502-214">Если это недоступно, используйте `serif` ".</span><span class="sxs-lookup"><span data-stu-id="19502-214">If that isn't available, use `serif`."</span></span>  

### <span data-ttu-id="19502-215">Добавление нескольких селекторов в набор правил</span><span class="sxs-lookup"><span data-stu-id="19502-215">Add multiple selectors to a ruleset</span></span>   

<span data-ttu-id="19502-216">Блок кода CSS вроде того, что вы видите ниже, называется набором **правил**.</span><span class="sxs-lookup"><span data-stu-id="19502-216">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="19502-217">Используйте запятые, чтобы добавить в набор правил несколько селекторов.</span><span class="sxs-lookup"><span data-stu-id="19502-217">Use commas to add multiple selectors to a ruleset.</span></span>  <span data-ttu-id="19502-218">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-218">Try it now:</span></span>  

1.  <span data-ttu-id="19502-219">На **вкладке Редактор**откройте `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-219">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="19502-220">После `li a` ввода `, h1` .</span><span class="sxs-lookup"><span data-stu-id="19502-220">After `li a` type `, h1`.</span></span>  

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

    <span data-ttu-id="19502-221">Таким образом браузер применяет `<h1>` элементы стиля так же, как и элементы, которые соответствуют шаблону `li a` .</span><span class="sxs-lookup"><span data-stu-id="19502-221">This tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="19502-222">Перейдите на **вкладку динамический**.</span><span class="sxs-lookup"><span data-stu-id="19502-222">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="19502-223">Щелкните ссылку **контакт** , чтобы вернуться на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="19502-223">Click the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="19502-224">Теперь **свяжитесь со мной!**</span><span class="sxs-lookup"><span data-stu-id="19502-224">Now, **Contact Me!**</span></span> <span data-ttu-id="19502-225">имеет тот же шрифт, что и ссылки для навигации.</span><span class="sxs-lookup"><span data-stu-id="19502-225">has the same font as the navigation links.</span></span>  
    
    > ##### <span data-ttu-id="19502-226">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="19502-226">Figure 11</span></span>  
    > <span data-ttu-id="19502-227">Текст "контактные данные!"</span><span class="sxs-lookup"><span data-stu-id="19502-227">The text 'Contact Me!'</span></span> <span data-ttu-id="19502-228">Теперь тот же шрифт, что и ссылки на домашнюю и контактный</span><span class="sxs-lookup"><span data-stu-id="19502-228">now has the same font as the Home and Contact links</span></span>  
    > ![Текстовые контакты!][ImageCssMultiple1]  

## <span data-ttu-id="19502-231">Поэкспериментировать с DevTools</span><span class="sxs-lookup"><span data-stu-id="19502-231">Experiment with DevTools</span></span>   

<span data-ttu-id="19502-232">По мере того как вы продолжите путешествие в главную веб-разработку, вы обнаружите, что эта таблица CSS может быть сложной.</span><span class="sxs-lookup"><span data-stu-id="19502-232">As you continue your journey to master web development, you'll find that CSS can be tricky.</span></span>  <span data-ttu-id="19502-233">Вы пишете некоторые стили CSS и ожидаете, что они будут отображаться одним из них, но браузер делает что-то совершенно другое.</span><span class="sxs-lookup"><span data-stu-id="19502-233">You'll write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="19502-234">Microsoft Edge DevTools упрощает эксперименты с изменениями и немедленно показывает, как эти изменения влияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="19502-234">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how those changes affect the page.</span></span>  

### <span data-ttu-id="19502-235">Добавление объявления к существующему правилу в DevTools</span><span class="sxs-lookup"><span data-stu-id="19502-235">Add a declaration to an existing rulest in DevTools</span></span>   

<span data-ttu-id="19502-236">Если вы хотите выполнить итерацию по стилю существующего элемента, добавьте объявление к существующему набору правил.</span><span class="sxs-lookup"><span data-stu-id="19502-236">When you want to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  <span data-ttu-id="19502-237">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-237">Try it now:</span></span>  

1.  <span data-ttu-id="19502-238">Щелкните ссылку " **Домашняя страница** " правой кнопкой мыши и выберите команду " **проверить**".</span><span class="sxs-lookup"><span data-stu-id="19502-238">Right-click the **Home** link and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="19502-239">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="19502-239">Figure 12</span></span>  
    > <span data-ttu-id="19502-240">Проверка ссылки на домашнюю страницу</span><span class="sxs-lookup"><span data-stu-id="19502-240">Inspecting the Home link</span></span>  
    > ![Проверка ссылки на домашнюю страницу][ImageCssAdd1]  
    
    <span data-ttu-id="19502-242">DevTools открывается вместе со страницей.</span><span class="sxs-lookup"><span data-stu-id="19502-242">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="19502-243">Код, представляющий ссылку на домашнюю страницу, `<a href="/">Home</a>` выделяется синим цветом в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="19502-243">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="19502-244">Это должно быть знакомо с тем, как начать [работу с HTML и DOM][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="19502-244">This should be familiar from [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>  <span data-ttu-id="19502-245">На вкладке " **стили** " под деревом DOM вы видите `font-family: 'Courier New', Courier, serif` объявление, которое вы добавили `contact.html` раньше.</span><span class="sxs-lookup"><span data-stu-id="19502-245">In the **Styles** tab below the DOM Tree you can see the `font-family: 'Courier New', Courier, serif` declaration that you added to `contact.html` earlier.</span></span>  
    
    > ##### <span data-ttu-id="19502-246">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="19502-246">Figure 13</span></span>  
    > <span data-ttu-id="19502-247">Вкладка "стили" находится под деревом DOM</span><span class="sxs-lookup"><span data-stu-id="19502-247">The Styles tab is below the DOM Tree</span></span>  
    > ![Вкладка "стили" находится под деревом DOM][ImageCssAdd2]  
    
    <span data-ttu-id="19502-249">Если окно DevTools является широкой страницей, вкладка стили находится справа от дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="19502-249">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="19502-250">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="19502-250">Figure 14</span></span>  
    > <span data-ttu-id="19502-251">Вкладка "стили" справа от дерева DOM</span><span class="sxs-lookup"><span data-stu-id="19502-251">The Styles tab is to the right of the DOM Tree</span></span>  
    > ![Вкладка "стили" справа от дерева DOM][ImageCssAdd3]  
    
1.  <span data-ttu-id="19502-253">Щелкните пробел ниже, `font-family: 'Courier New', Courier, Serif` чтобы добавить новое объявление.</span><span class="sxs-lookup"><span data-stu-id="19502-253">Click the whitespace below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    > ##### <span data-ttu-id="19502-254">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="19502-254">Figure 15</span></span>  
    > <span data-ttu-id="19502-255">Добавление нового объявления</span><span class="sxs-lookup"><span data-stu-id="19502-255">Adding a new declaration</span></span>  
    > ![Добавление нового объявления][ImageCssAdd4]  
    
1.  <span data-ttu-id="19502-257">Введите текст `color` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="19502-257">Type `color` and then press `Enter`.</span></span>  <span data-ttu-id="19502-258">Пользовательский интерфейс автозаполнения предлагает параметры по мере ввода.</span><span class="sxs-lookup"><span data-stu-id="19502-258">The autocomplete UI suggests options as you type.</span></span>  
    
    > ##### <span data-ttu-id="19502-259">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="19502-259">Figure 16</span></span>  
    > <span data-ttu-id="19502-260">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="19502-260">Typing</span></span> `color`  
    > ![Цвет текста][ImageCssAdd5]  

1.  <span data-ttu-id="19502-262">Введите текст `magenta` и нажмите `Enter` еще раз.</span><span class="sxs-lookup"><span data-stu-id="19502-262">Type `magenta` and then press `Enter` again.</span></span>  <span data-ttu-id="19502-263">Весь текст на странице контакта стал пурпурным.</span><span class="sxs-lookup"><span data-stu-id="19502-263">All of the text on the contact page is now magenta.</span></span>  
    
    > ##### <span data-ttu-id="19502-264">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="19502-264">Figure 17</span></span>  
    > <span data-ttu-id="19502-265">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="19502-265">Typing</span></span> `magenta`  
    > ![Ввод пурпурного][ImageCssAdd6]  
    
### <span data-ttu-id="19502-267">Изменение объявления в DevTools</span><span class="sxs-lookup"><span data-stu-id="19502-267">Edit a declaration in DevTools</span></span>   

<span data-ttu-id="19502-268">Вы также можете изменить существующие объявления в DevTools.</span><span class="sxs-lookup"><span data-stu-id="19502-268">You can also edit existing declarations in DevTools.</span></span>  <span data-ttu-id="19502-269">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-269">Try it now:</span></span>  

1.  <span data-ttu-id="19502-270">Щелкните пурпурный квадрат рядом с `magenta` .</span><span class="sxs-lookup"><span data-stu-id="19502-270">Click the magenta square next to `magenta`.</span></span>  <span data-ttu-id="19502-271">Появится палитра выбора цвета.</span><span class="sxs-lookup"><span data-stu-id="19502-271">A color picker pops up.</span></span>  
    
    > ##### <span data-ttu-id="19502-272">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="19502-272">Figure 18</span></span>  
    > <span data-ttu-id="19502-273">Выбор цвета</span><span class="sxs-lookup"><span data-stu-id="19502-273">The Color Picker</span></span>  
    > ![Выбор цвета][ImageCssEdit1]  
    
1.  <span data-ttu-id="19502-275">С помощью средства выбора цвета измените текст шрифта на нужный цвет.</span><span class="sxs-lookup"><span data-stu-id="19502-275">Use the color picker to change the font text to a color that you like.</span></span>  
    
    > ##### <span data-ttu-id="19502-276">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="19502-276">Figure 19</span></span>  
    > <span data-ttu-id="19502-277">Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="19502-277">Changing the font color to purple with the Color Picker</span></span>  
    > ![Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета][ImageCssEdit2]  

### <span data-ttu-id="19502-279">Добавление нового набора правил в DevTools</span><span class="sxs-lookup"><span data-stu-id="19502-279">Add a new ruleset in DevTools</span></span>   

<span data-ttu-id="19502-280">Вы также можете добавлять новые наборы правил в DevTools.</span><span class="sxs-lookup"><span data-stu-id="19502-280">You can also add new rulesets in DevTools.</span></span>  <span data-ttu-id="19502-281">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-281">Try it now:</span></span>  

1.  <span data-ttu-id="19502-282">Нажмите **новое правило стиля** ![ новое правило стиля ][ImageNewStyleRuleIcon] , которое находится рядом с полем **CLS**.</span><span class="sxs-lookup"><span data-stu-id="19502-282">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] which is next to **.cls**.</span></span>  <span data-ttu-id="19502-283">В качестве Selector появится пустой набор правил `a` .</span><span class="sxs-lookup"><span data-stu-id="19502-283">An empty ruleset appears with `a` as the selector.</span></span>  
    
    > ##### <span data-ttu-id="19502-284">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="19502-284">Figure 20</span></span>  
    > <span data-ttu-id="19502-285">Добавление нового правила</span><span class="sxs-lookup"><span data-stu-id="19502-285">Adding a new rule</span></span>  
    > ![Добавление нового правила][ImageCssRule1]  
    
1.  <span data-ttu-id="19502-287">Заменить `a` на `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="19502-287">Replace `a` with `a:hover`.</span></span>  
    
    > ##### <span data-ttu-id="19502-288">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="19502-288">Figure 21</span></span>  
    > <span data-ttu-id="19502-289">Замена `a` на</span><span class="sxs-lookup"><span data-stu-id="19502-289">Replacing `a` with</span></span> `a:hover`  
    > ![Замена в a:hover][ImageCssRule2]  
    
    `:hover` <span data-ttu-id="19502-291">является **псевдо-классом**.</span><span class="sxs-lookup"><span data-stu-id="19502-291">is a **pseudo-class**.</span></span>  <span data-ttu-id="19502-292">Используйте псевдо-классы для стиля элементов при вводе специальных состояний.</span><span class="sxs-lookup"><span data-stu-id="19502-292">Use pseudo-classes to style elements when they enter special states.</span></span>  <span data-ttu-id="19502-293">Например, `a:hover` стиль вступает в силу только при наведении указателя мыши на `<a>` элемент.</span><span class="sxs-lookup"><span data-stu-id="19502-293">For example, the `a:hover` style only takes effect when you're hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="19502-294">Щелкните между скобками, чтобы добавить новое объявление.</span><span class="sxs-lookup"><span data-stu-id="19502-294">Click between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="19502-295">Введите `background-color` имя объявления и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="19502-295">Type `background-color` for the declaration name and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="19502-296">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="19502-296">Figure 22</span></span>  
    > <span data-ttu-id="19502-297">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="19502-297">Typing</span></span> `background-color`  
    > ![Ввод цвета фона][ImageCssRule3]  
    
1.  <span data-ttu-id="19502-299">Введите `green` значение объявления и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="19502-299">Type `green` for the declaration value and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="19502-300">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="19502-300">Figure 23</span></span>  
    > <span data-ttu-id="19502-301">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="19502-301">Typing</span></span> `green`  
    > ![Ввод зеленого][ImageCssRule4]  
    
1.  <span data-ttu-id="19502-303">Наведите указатель мыши на ссылку " **Домашняя страница** ".</span><span class="sxs-lookup"><span data-stu-id="19502-303">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="19502-304">Фон ссылки становится зеленым.</span><span class="sxs-lookup"><span data-stu-id="19502-304">The background of the link turns green.</span></span>  
    
    > ##### <span data-ttu-id="19502-305">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="19502-305">Figure 24</span></span>  
    > <span data-ttu-id="19502-306">Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон.</span><span class="sxs-lookup"><span data-stu-id="19502-306">Hovering over the Home link to reveal its green background</span></span>  
    > ![Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон.][ImageCssRule5]  
    
## <span data-ttu-id="19502-308">Повторное использование стилей на разных страницах с внешними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="19502-308">Re-use styles across pages with external stylesheets</span></span>   

<span data-ttu-id="19502-309">Ранее вы добавили эту внутреннюю таблицу стилей в `contact.html` :</span><span class="sxs-lookup"><span data-stu-id="19502-309">Earlier you added this internal stylesheet to `contact.html`:</span></span>  

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

<span data-ttu-id="19502-310">Что делать, если вы захотите стиль `index.html` одинаково?</span><span class="sxs-lookup"><span data-stu-id="19502-310">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="19502-311">Что делать, если у вас *тысячи* страниц и вы хотите применить эти стили ко всем из них?</span><span class="sxs-lookup"><span data-stu-id="19502-311">What if you had a *thousand* pages and you wanted to apply these styles to all of them?</span></span>  <span data-ttu-id="19502-312">Вам потребуется скопировать и вставить этот внутренний набор таблиц в каждую веб-страницу на сайте.</span><span class="sxs-lookup"><span data-stu-id="19502-312">You'd have to copy and paste this internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="19502-313">**Внешние таблицы стилей** позволяют создавать CSS, пока они применены к нескольким страницам.</span><span class="sxs-lookup"><span data-stu-id="19502-313">**External stylesheets** allow you to write your CSS once yet apply it to multiple pages.</span></span>  <span data-ttu-id="19502-314">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-314">Try it now:</span></span>  

1.  <span data-ttu-id="19502-315">Сначала перезагрузите вкладку Live, чтобы удалить изменения, внесенные в DevTools.</span><span class="sxs-lookup"><span data-stu-id="19502-315">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    > ##### <span data-ttu-id="19502-316">Рис. 25</span><span class="sxs-lookup"><span data-stu-id="19502-316">Figure 25</span></span>  
    >  <span data-ttu-id="19502-317">После перезагрузки страницы изменения, внесенные в DevTools, исчезают</span><span class="sxs-lookup"><span data-stu-id="19502-317">After reloading the page the changes that were made in DevTools are gone</span></span>  
    > ![ <span data-ttu-id="19502-318">После перезагрузки страницы изменения, внесенные в DevTools, исчезают</span><span class="sxs-lookup"><span data-stu-id="19502-318">After reloading the page the changes that were made in DevTools are gone</span></span>][ImageCssExternal01]  
    
1.  <span data-ttu-id="19502-319">Вернитесь на **вкладку Редактор** и откройте ее `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-319">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="19502-320">Рис. 26</span><span class="sxs-lookup"><span data-stu-id="19502-320">Figure 26</span></span>  
    > `contact.html`  
    > ![contact.html][ImageCssExternal02]  
    
1.  <span data-ttu-id="19502-322">Удалить все между `<style>` и `</style>` , включая `<style>` и `</style>` .</span><span class="sxs-lookup"><span data-stu-id="19502-322">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    > ##### <span data-ttu-id="19502-323">На рисунке 27</span><span class="sxs-lookup"><span data-stu-id="19502-323">Figure 27</span></span>  
    > <span data-ttu-id="19502-324">Тег Style был удален</span><span class="sxs-lookup"><span data-stu-id="19502-324">The style tag has been removed</span></span>  
    > ![Тег Style был удален][ImageCssExternal03]  
    
1.  <span data-ttu-id="19502-326">Перейдите к `index.html` тегу и удалите `style="background-color: aliceblue;"` его `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="19502-326">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="19502-327">Теперь вы удалили все CSS-таблицы, которые вы ранее добавили на сайт.</span><span class="sxs-lookup"><span data-stu-id="19502-327">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    > ##### <span data-ttu-id="19502-328">Рис. 28</span><span class="sxs-lookup"><span data-stu-id="19502-328">Figure 28</span></span>  
    > <span data-ttu-id="19502-329">Встроенный стиль удален из элемента навигации</span><span class="sxs-lookup"><span data-stu-id="19502-329">The inline style has been removed from the nav element</span></span>  
    > ![Встроенный стиль удален из элемента навигации][ImageCssExternal04]  

1.  <span data-ttu-id="19502-331">Нажмите кнопку **создать файл**.</span><span class="sxs-lookup"><span data-stu-id="19502-331">Click **New File**.</span></span>  
    
    > ##### <span data-ttu-id="19502-332">Рис. 29</span><span class="sxs-lookup"><span data-stu-id="19502-332">Figure 29</span></span>  
    > <span data-ttu-id="19502-333">Диалоговое окно "Создание файла"</span><span class="sxs-lookup"><span data-stu-id="19502-333">The new file dialog</span></span>  
    > ![Диалоговое окно "Создание файла"][ImageCssExternal05]  
    
1.  <span data-ttu-id="19502-335">Замените `cool-file.js` на `style.css` и нажмите кнопку **Добавить файл**.</span><span class="sxs-lookup"><span data-stu-id="19502-335">Replace `cool-file.js` with `style.css` and then click **Add File**.</span></span>  
    
    > ##### <span data-ttu-id="19502-336">Рис. 30</span><span class="sxs-lookup"><span data-stu-id="19502-336">Figure 30</span></span>  
    > <span data-ttu-id="19502-337">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="19502-337">Typing</span></span> `style.css`  
    > ![Ввод Style. CSS][ImageCssExternal06]  
    
1.  <span data-ttu-id="19502-339">Вставьте этот код в `style.css` :</span><span class="sxs-lookup"><span data-stu-id="19502-339">Paste this code into `style.css`:</span></span>  
    
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
    
    > ##### <span data-ttu-id="19502-340">На рисунке 31</span><span class="sxs-lookup"><span data-stu-id="19502-340">Figure 31</span></span>  
    > <span data-ttu-id="19502-341">Добавление кода в</span><span class="sxs-lookup"><span data-stu-id="19502-341">Adding code to</span></span> `style.css`  
    > ![Добавление кода в Style. CSS][ImageCssExternal07]  
    
    <span data-ttu-id="19502-343">На этом этапе вы создали внешнюю таблицу стилей, но ваш HTML-код еще не знает, что он существует.</span><span class="sxs-lookup"><span data-stu-id="19502-343">At this point, you have created an external stylesheet, but your HTML doesn't know that it exists, yet.</span></span>  
    
1.  <span data-ttu-id="19502-344">Open (открыть) `index.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-344">Open `index.html`.</span></span>  
1.  <span data-ttu-id="19502-345">Добавьте `<link rel="stylesheet" href="style.css">` в свой HTML-код.</span><span class="sxs-lookup"><span data-stu-id="19502-345">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### <span data-ttu-id="19502-346">Рисунок 32</span><span class="sxs-lookup"><span data-stu-id="19502-346">Figure 32</span></span>  
    > <span data-ttu-id="19502-347">Связывание с</span><span class="sxs-lookup"><span data-stu-id="19502-347">Linking to</span></span> `style.css`  
    > ![Связывание с Style. CSS][ImageCssExternal08]  

1.  <span data-ttu-id="19502-349">Перейдите к разделу `contact.html` и добавьте в него ссылку.</span><span class="sxs-lookup"><span data-stu-id="19502-349">Go to `contact.html` and add the link there, too.</span></span>  
    
    > ##### <span data-ttu-id="19502-350">Рисунок 33</span><span class="sxs-lookup"><span data-stu-id="19502-350">Figure 33</span></span>  
    > <span data-ttu-id="19502-351">Связывание `style.css` в</span><span class="sxs-lookup"><span data-stu-id="19502-351">Linking to `style.css` in</span></span> `contact.html`  
    > ![Связывание со стилем Style. CSS в contact.html][ImageCssExternal09]  

1.  <span data-ttu-id="19502-353">Перейдите на **вкладку динамический**.  Домашняя страница теперь имеет тот же шрифт, что и в последнем разделе, и в синем разделе навигации.</span><span class="sxs-lookup"><span data-stu-id="19502-353">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    > ##### <span data-ttu-id="19502-354">Рисунок 34</span><span class="sxs-lookup"><span data-stu-id="19502-354">Figure 34</span></span>  
    > <span data-ttu-id="19502-355">Домашняя страница</span><span class="sxs-lookup"><span data-stu-id="19502-355">The home page</span></span>  
    > ![Домашняя страница][ImageCssExternal10]  
    
1.  <span data-ttu-id="19502-357">Щелкните ссылку **контакт** , чтобы перейти на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="19502-357">Click the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="19502-358">Страница контакта имеет тот же формат, что и домашняя страница.</span><span class="sxs-lookup"><span data-stu-id="19502-358">The contact page has the same formatting as the home page.</span></span>  
    
    > ##### <span data-ttu-id="19502-359">Рисунок 35</span><span class="sxs-lookup"><span data-stu-id="19502-359">Figure 35</span></span>  
    > <span data-ttu-id="19502-360">Страница "контакт"</span><span class="sxs-lookup"><span data-stu-id="19502-360">The contact page</span></span>  
    > ![Страница "контакт"][ImageCssExternal11]  
    
## <span data-ttu-id="19502-362">Использование платформы CSS</span><span class="sxs-lookup"><span data-stu-id="19502-362">Use a CSS framework</span></span>   

<span data-ttu-id="19502-363">**Платформы CSS** — это коллекции стилей, разработанных другими разработчиками, которые упрощают создание привлекательных веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="19502-363">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="19502-364">Вместо того чтобы определять стили самостоятельно, платформа предоставляет коллекцию стилей, которые можно использовать в элементах страницы.</span><span class="sxs-lookup"><span data-stu-id="19502-364">Instead of defining styles yourself, a framework gives you a collection of styles that you can use on your page elements.</span></span>  

1.  <span data-ttu-id="19502-365">Скопируйте приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="19502-365">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="19502-366">Перейдите на вкладку Правка и вставьте код в `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-366">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="19502-367">Рисунок 36</span><span class="sxs-lookup"><span data-stu-id="19502-367">Figure 36</span></span>  
    > <span data-ttu-id="19502-368">Связывание с платформой в</span><span class="sxs-lookup"><span data-stu-id="19502-368">Linking to the framework in</span></span> `contact.html`  
    > ![Связывание с платформой в contact.html][ImageCssFramework1]  
    
1.  <span data-ttu-id="19502-370">Также вставьте код в `index.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-370">Paste the code into `index.html`, as well.</span></span>  
    
    > ##### <span data-ttu-id="19502-371">Рисунок 37</span><span class="sxs-lookup"><span data-stu-id="19502-371">Figure 37</span></span>  
    > <span data-ttu-id="19502-372">Связывание с платформой в</span><span class="sxs-lookup"><span data-stu-id="19502-372">Linking to the framework in</span></span> `index.html`  
    > ![Связывание с платформой в index.html][ImageCssFramework2]  
    
1.  <span data-ttu-id="19502-374">Вернитесь на вкладку динамический, чтобы просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="19502-374">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="19502-375">Несмотря на то, что цвет фона `<nav>` и шрифт элементов совпадают `li a` , изменился шрифт других элементов.</span><span class="sxs-lookup"><span data-stu-id="19502-375">While the background color of the `<nav>` and the font of the `li a` elements are the same, the font of the other elements has changed.</span></span>  
    
    > ##### <span data-ttu-id="19502-376">Рисунок 38</span><span class="sxs-lookup"><span data-stu-id="19502-376">Figure 38</span></span>  
    > <span data-ttu-id="19502-377">Некоторые шрифты на домашней странице изменились из-за платформы</span><span class="sxs-lookup"><span data-stu-id="19502-377">Some of the font on the home page has changed because of the framework</span></span>  
    > ![Некоторые шрифты на домашней странице изменились из-за платформы][ImageCssFramework3]  

### <span data-ttu-id="19502-379">Использование класса</span><span class="sxs-lookup"><span data-stu-id="19502-379">Use a class</span></span>   

<span data-ttu-id="19502-380">В последнем разделе вы добавили начальную загрузку на веб-страницы, которая изменила шрифты для некоторых элементов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="19502-380">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="19502-381">Структуры CSS помогают вносить существенные изменения на странице с помощью очень небольшого количества кода.</span><span class="sxs-lookup"><span data-stu-id="19502-381">CSS frameworks can help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="19502-382">Попробуйте выполнить его прямо сейчас, изменив верхний колонтитул:</span><span class="sxs-lookup"><span data-stu-id="19502-382">Try it now by changing your header:</span></span>  

1.  <span data-ttu-id="19502-383">Скопируйте этот код:</span><span class="sxs-lookup"><span data-stu-id="19502-383">Copy this code:</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="19502-384">Добавьте этот код в `<header>` тег в `index.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-384">Add this code to your `<header>` tag in `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="19502-385">Рисунок 39</span><span class="sxs-lookup"><span data-stu-id="19502-385">Figure 39</span></span>  
    > <span data-ttu-id="19502-386">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="19502-386">Adding classes in</span></span> `index.html`  
    > ![Добавление классов в index.html][ImageCssJumbotron1]  
    
1.  <span data-ttu-id="19502-388">Добавьте код в `<header>` тег `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-388">Add the code to your `<header>` tag in `contact.html`, too.</span></span>  
    
    > ##### <span data-ttu-id="19502-389">Рисунок 40</span><span class="sxs-lookup"><span data-stu-id="19502-389">Figure 40</span></span>  
    > <span data-ttu-id="19502-390">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="19502-390">Adding classes in</span></span> `contact.html`  
    > ![Добавление классов в contact.html][ImageCssJumbotron2]  
    
1.  <span data-ttu-id="19502-392">Просмотрите изменения на вкладке "живые".  На вашем заголовке есть большое затененное поле.</span><span class="sxs-lookup"><span data-stu-id="19502-392">View your changes in the live tab.  There's a big, grey box around your header now.</span></span>  
    
    > ##### <span data-ttu-id="19502-393">Рисунок 41</span><span class="sxs-lookup"><span data-stu-id="19502-393">Figure 41</span></span>  
    > <span data-ttu-id="19502-394">Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него.</span><span class="sxs-lookup"><span data-stu-id="19502-394">The header now has a big, grey box around it</span></span>  
    > ![Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него.][ImageCssJumbotron3]  
    
### <span data-ttu-id="19502-396">Общие сведения о классах</span><span class="sxs-lookup"><span data-stu-id="19502-396">Understand classes</span></span>   

<span data-ttu-id="19502-397">Классы позволяют назначать коллекции стилей произвольным элементам.</span><span class="sxs-lookup"><span data-stu-id="19502-397">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="19502-398">Например, установка `class` атрибута `<header>` тегов для `jumbotron` применения к ним указанных ниже стилей.</span><span class="sxs-lookup"><span data-stu-id="19502-398">For example, setting the `class` attribute of the `<header>` tags to `jumbotron` applied the following styles to them:</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="19502-399">Одно из преимуществ классов состоит в том, что они позволяют применять стили к любым нужным элементам.</span><span class="sxs-lookup"><span data-stu-id="19502-399">One advantage of classes is that they let you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="19502-400">Например, предположим, что вы хотите установить для *некоторых* `<p>` элементов цвет фона, который будет фиолетовым, но не *всеми* .</span><span class="sxs-lookup"><span data-stu-id="19502-400">For example, suppose you want to set the background color of *some* `<p>` elements to purple, but not *all* of them.</span></span>  <span data-ttu-id="19502-401">Вы можете определить стиль в классе.</span><span class="sxs-lookup"><span data-stu-id="19502-401">You could define the style in a class:</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="19502-402">А затем примените этот класс только к `<p>` элементам, которые вы хотите отформатировать:</span><span class="sxs-lookup"><span data-stu-id="19502-402">And then apply the class to only the `<p>` elements that you want to style:</span></span>  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### <span data-ttu-id="19502-403">Выравнивание элементов</span><span class="sxs-lookup"><span data-stu-id="19502-403">Align elements</span></span>   

<span data-ttu-id="19502-404">Начальная загрузка также предоставляет классы для выравнивания элементов.</span><span class="sxs-lookup"><span data-stu-id="19502-404">Bootstrap also provides classes for aligning elements.</span></span>  <span data-ttu-id="19502-405">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="19502-405">Try it now:</span></span>  

1.  <span data-ttu-id="19502-406">Вернитесь на вкладку Редактор и откройте ее `index.html` .</span><span class="sxs-lookup"><span data-stu-id="19502-406">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="19502-407">Добавьте `class="container-fluid"` в свой `<body>` тег.</span><span class="sxs-lookup"><span data-stu-id="19502-407">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    > ##### <span data-ttu-id="19502-408">Рисунок 42</span><span class="sxs-lookup"><span data-stu-id="19502-408">Figure 42</span></span>  
    > <span data-ttu-id="19502-409">Добавление `container-fluid` класса</span><span class="sxs-lookup"><span data-stu-id="19502-409">Adding the `container-fluid` class</span></span>  
    > ![Добавление класса Container-жидкости][ImageCssAlign1]  

1.  <span data-ttu-id="19502-411">Обтекание `<nav>` `<main>` элементов `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="19502-411">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="19502-412">`</div>`Чтобы правильно закрыть новый тег, убедитесь в том, что вы хотите сделать `</main>` это.</span><span class="sxs-lookup"><span data-stu-id="19502-412">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    > ##### <span data-ttu-id="19502-413">Рисунок 43</span><span class="sxs-lookup"><span data-stu-id="19502-413">Figure 43</span></span>  
    > <span data-ttu-id="19502-414">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="19502-414">Adding a row</span></span>  
    > ![Добавление строки][ImageCssAlign2]  
    
1.  <span data-ttu-id="19502-416">Добавьте `class="col-3"` теги в тег `<nav>` и `class="col-9"` в `<main>` тег.</span><span class="sxs-lookup"><span data-stu-id="19502-416">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    > ##### <span data-ttu-id="19502-417">Рисунок 44</span><span class="sxs-lookup"><span data-stu-id="19502-417">Figure 44</span></span>  
    > <span data-ttu-id="19502-418">Добавление `col-3` и использование `col-9` классов</span><span class="sxs-lookup"><span data-stu-id="19502-418">Adding the `col-3` and `col-9` classes</span></span>  
    > ![Добавление классов Col-3 и Col-9][ImageCssAlign3]  
    
1.  <span data-ttu-id="19502-420">Просмотрите изменения на вкладке "живые".</span><span class="sxs-lookup"><span data-stu-id="19502-420">View your changes in the live tab.</span></span>  
    
    > ##### <span data-ttu-id="19502-421">Рисунок 45</span><span class="sxs-lookup"><span data-stu-id="19502-421">Figure 45</span></span>  
    > <span data-ttu-id="19502-422">Содержимое элемента навигации теперь находится слева от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="19502-422">The nav content is now to the left of the main content</span></span>  
    > ![Содержимое элемента навигации теперь находится слева от основного содержимого.][ImageCssAlign4]  
    
## <span data-ttu-id="19502-424">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="19502-424">Next steps</span></span>   

<span data-ttu-id="19502-425">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="19502-425">Congratulations!</span></span>  <span data-ttu-id="19502-426">Готово!</span><span class="sxs-lookup"><span data-stu-id="19502-426">You're done!</span></span>  

*   <span data-ttu-id="19502-427">Лучший способ улучшить качество веб-приложений — создать дополнительные сайты.</span><span class="sxs-lookup"><span data-stu-id="19502-427">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="19502-428">Не беспокойтесь о нарушениях.</span><span class="sxs-lookup"><span data-stu-id="19502-428">Don't worry about breaking stuff.</span></span>  <span data-ttu-id="19502-429">Просто восприяты и намерены очень удобно.</span><span class="sxs-lookup"><span data-stu-id="19502-429">Just have fun and learn as much as you can along the way.</span></span>  
*   <span data-ttu-id="19502-430">Ознакомьтесь со статьей [Введение в CSS][MDNCssFirstSteps] , чтобы узнать больше о стилях веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="19502-430">Check out [Introduction to CSS][MDNCssFirstSteps] to learn lots more about styling web pages.</span></span>  
*   <span data-ttu-id="19502-431">Узнайте больше о том, как можно использовать DevTools для экспериментов с CSS [-таблицей][DevtoolsCssIndex] .</span><span class="sxs-lookup"><span data-stu-id="19502-431">Work through our [Get Started with Viewing and Changing CSS][DevtoolsCssIndex] tutorial to learn more about how you can use DevTools to experiment with a page's CSS.</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Рисунок 1: как выглядит ваш сайт"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "На рисунке 2 показано, как будет выглядеть ваш сайт в конце учебника."  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Рисунок 3: вкладка "Редактирование""  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Рисунок 4: меню "Параметры проекта""  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Рисунок 5. Вкладка "динамический""  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Рисунок 6: этот стиль помечен с помощью CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Рисунок 7: index.html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Рисунок 8: цвет фона, на котором находятся ссылки на домашнюю и контактный, теперь синего цвета"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Рисунок 9: страница "контакт""  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Рисунок 10: изменен шрифт ссылок на домашнюю и контактный"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Рисунок 11: текст "контактные данные" теперь имеет тот же шрифт, что и ссылки на домашнюю и контактный."  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Рисунок 12: Проверка ссылки на домашнюю страницу"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Рисунок 13. Вкладка "стили" находится под деревом DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Рисунок 14: вкладка "стили" справа от дерева DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Рисунок 15: Добавление нового объявления"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Рисунок 16: ввод цвета"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Рисунок 17: ввод пурпурного"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Рисунок 18: палитра цветов"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "На рисунке 19 показано, как изменить цвет шрифта на фиолетовый с помощью палитры цветов."  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Рисунок 20: Добавление нового правила"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Рисунок 21: Замена a на a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Рисунок 22: ввод цвета фона"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Рисунок 23: ввод зеленого"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Рис. 24: наведение указателя мыши на домашнюю ссылку для отображения зеленого фона"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Рис. 25: после перезагрузки страницы изменения, внесенные в DevTools, исчезают"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Рисунок 26: contact.html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Рисунок 27: тег Style был удален"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Рис. 28: встроенный стиль удален из элемента навигации."  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Рис. 29: диалоговое окно "Создание файла""  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Рисунок 30: ввод Style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Рисунок 31: Добавление кода в Style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Рисунок 32: связывание со стилем Style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Рисунок 33: связывание со стилем Style. CSS в contact.html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Рисунок 34: Главная страница"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Рисунок 35: страница контакта"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Рисунок 36: связывание с платформой в contact.html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Рисунок 37: связывание с платформой в index.html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Рисунок 38: некоторые шрифты на домашней странице изменились из-за платформы"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Рисунок 39: Добавление классов в index.html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Рисунок 40: Добавление классов в contact.html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Рисунок 41: теперь верхний колонтитул имеет большой серый прямоугольник вокруг него."  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Рисунок 42: Добавление класса Container-жидкостный"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Рисунок 43: Добавление строки"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Рисунок 44: Добавление классов Col-3 и Col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Рисунок 45: содержимое элемента навигации теперь находится слева от основного содержимого."  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools для начинающих: Приступая к работе с HTML и моделью DOM"  
[DevtoolsCssIndex]: ../css/index.md "Приступая к просмотру и изменению каскадных таблиц стилей"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-готовил-amphibian | Цепь"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Первые шаги CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="19502-482">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19502-482">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="19502-483">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/css) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="19502-483">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="19502-485">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19502-485">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  

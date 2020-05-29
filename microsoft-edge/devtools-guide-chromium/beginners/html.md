---
title: DevTools для начинающих
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 8695fe1b2c5d78bd074447acd26a1f01a5833b2d
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581589"
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

# <span data-ttu-id="114b9-103">DevTools для начинающих: Приступая к работе с HTML и моделью DOM</span><span class="sxs-lookup"><span data-stu-id="114b9-103">DevTools for Beginners: Get Started with HTML and the DOM</span></span>   

<span data-ttu-id="114b9-104">Это первый из ряда учебников, в котором изучаются основы разработки веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="114b9-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="114b9-105">Кроме того, вы узнаете о наборе средств для веб-разработчиков, именуемых Microsoft Edge DevTools, которые могут повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="114b9-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="114b9-106">В этом конкретном учебнике вы узнаете о HTML и модели DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="114b9-107">HTML — это одна из основных методик разработки веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="114b9-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="114b9-108">Это язык, управляющий структурой и содержимым веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="114b9-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="114b9-109">Модель DOM также связана со структурой и контентом веб-страниц, но вы узнаете об этом позже.</span><span class="sxs-lookup"><span data-stu-id="114b9-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="114b9-110">Цели</span><span class="sxs-lookup"><span data-stu-id="114b9-110">Goals</span></span>   

<span data-ttu-id="114b9-111">Вы собираетесь познакомиться с веб-разработкой, завершив создание собственного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="114b9-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="114b9-112">Завершив все учебные курсы в серии *DevTools для начинающих* , ваш готовый веб-сайт будет выглядеть так, как **показано на рисунке 1**.</span><span class="sxs-lookup"><span data-stu-id="114b9-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like **Figure 1**.</span></span>  

> ##### <span data-ttu-id="114b9-113">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="114b9-113">Figure 1</span></span>  
> <span data-ttu-id="114b9-114">Готовый сайт</span><span class="sxs-lookup"><span data-stu-id="114b9-114">The finished site</span></span>  
> ![Готовый сайт][ImageHtmlFinished]  

<span data-ttu-id="114b9-116">В конце этого учебника вы узнаете:</span><span class="sxs-lookup"><span data-stu-id="114b9-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="114b9-117">Как HTML и DOM создают содержимое, которое отображается на веб-страницах.</span><span class="sxs-lookup"><span data-stu-id="114b9-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="114b9-118">Как Microsoft Edge DevTools помогает экспериментировать с изменениями HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="114b9-119">Разница между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="114b9-120">У тебя также есть реальный веб-сайт!</span><span class="sxs-lookup"><span data-stu-id="114b9-120">You'll also have a real website!</span></span>  <span data-ttu-id="114b9-121">Вы можете использовать этот сайт для размещения резюме или блога.</span><span class="sxs-lookup"><span data-stu-id="114b9-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="114b9-122">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="114b9-122">Prerequisites</span></span>   

<span data-ttu-id="114b9-123">Прежде чем приступить к работе с учебником, выполните следующие требования:</span><span class="sxs-lookup"><span data-stu-id="114b9-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="114b9-124">Если вы не знакомы с форматом HTML, ознакомьтесь с разделом начало [работы с HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="114b9-124">If you're unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="114b9-125">Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="114b9-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="114b9-126">В этом учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="114b9-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="114b9-127">Настройка кода</span><span class="sxs-lookup"><span data-stu-id="114b9-127">Set up your code</span></span>   

<span data-ttu-id="114b9-128">Вы собираетесь создать сайт в редакторе кода на веб-сайте с именем "сбой".</span><span class="sxs-lookup"><span data-stu-id="114b9-128">You're going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="114b9-129">Откройте [Исходный код][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="114b9-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="114b9-130">Эта вкладка будет называться **вкладкой "редактор"** в рамках этого учебника.</span><span class="sxs-lookup"><span data-stu-id="114b9-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    > ##### <span data-ttu-id="114b9-131">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="114b9-131">Figure 2</span></span>  
    > <span data-ttu-id="114b9-132">Вкладка "редактор"</span><span class="sxs-lookup"><span data-stu-id="114b9-132">The editor tab</span></span>  
    > ![Вкладка "редактор"][ImageHtmlSetup1]  

1.  <span data-ttu-id="114b9-134">Щелкните **alluring-удар**.</span><span class="sxs-lookup"><span data-stu-id="114b9-134">Click **alluring-shock**.</span></span>  <span data-ttu-id="114b9-135">В левом верхнем углу откроется меню "Параметры проекта".</span><span class="sxs-lookup"><span data-stu-id="114b9-135">The Project Options menu opens in the top-left corner.</span></span>  
    
    > #### <span data-ttu-id="114b9-136">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="114b9-136">Figure 3</span></span>  
    > <span data-ttu-id="114b9-137">Меню "Параметры проекта"</span><span class="sxs-lookup"><span data-stu-id="114b9-137">The Project Options menu</span></span>  
    > ![Меню "Параметры проекта"][ImageHtmlSetup2]  
    
1.  <span data-ttu-id="114b9-139">Щелкните **Remix Project (проект**).</span><span class="sxs-lookup"><span data-stu-id="114b9-139">Click **Remix Project**.</span></span>  <span data-ttu-id="114b9-140">При возникновении недостаточной версии создается копия проекта, которую можно редактировать и случайным образом создает новое имя для проекта.</span><span class="sxs-lookup"><span data-stu-id="114b9-140">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="114b9-141">Содержимое будет таким же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="114b9-141">The content is the same as before.</span></span>  
    
    > ##### <span data-ttu-id="114b9-142">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="114b9-142">Figure 4</span></span>  
    > <span data-ttu-id="114b9-143">Смешанный проект</span><span class="sxs-lookup"><span data-stu-id="114b9-143">The remixed project</span></span>  
    > ![Смешанный проект][ImageHtmlSetup3]  
    
1.  <span data-ttu-id="114b9-145">Если вы планируете выполнить следующий учебник в этой серии, нажмите **Вход** и войдите в систему, чтобы завершить работу с учетной записью GitHub или Facebook.</span><span class="sxs-lookup"><span data-stu-id="114b9-145">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="114b9-146">Если вы не входите в свою учетную запись, то после закрытия вкладки Правка вы потеряли возможность изменить этот проект.</span><span class="sxs-lookup"><span data-stu-id="114b9-146">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="114b9-147">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="114b9-147">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="114b9-148">Откроется новая вкладка, на которой отображается активная страница.</span><span class="sxs-lookup"><span data-stu-id="114b9-148">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="114b9-149">Эта вкладка будет называться на **вкладке динамический** в рамках этого учебника.</span><span class="sxs-lookup"><span data-stu-id="114b9-149">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="114b9-150">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="114b9-150">Figure 5</span></span>  
    > <span data-ttu-id="114b9-151">Вкладка "динамический"</span><span class="sxs-lookup"><span data-stu-id="114b9-151">The live tab</span></span>  
    > ![Вкладка "динамический"][ImageHtmlSetup4]  
    
## <span data-ttu-id="114b9-153">Добавление содержимого</span><span class="sxs-lookup"><span data-stu-id="114b9-153">Add content</span></span>   

<span data-ttu-id="114b9-154">Ваш сайт совершенно пуст.</span><span class="sxs-lookup"><span data-stu-id="114b9-154">Your site is pretty empty.</span></span>  <span data-ttu-id="114b9-155">Чтобы добавить содержимое, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="114b9-155">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="114b9-156">На **вкладке "редактор"** замените `<!-- You're "About Me" will go here.  -->` на `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="114b9-156">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="114b9-157">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="114b9-157">Figure 6</span></span>  
    > <span data-ttu-id="114b9-158">На вкладке "редактор" выделена новая программа</span><span class="sxs-lookup"><span data-stu-id="114b9-158">The new code is highlighted in the editor tab</span></span>  
    > ![На вкладке "редактор" выделена новая программа][ImageHtmlAdd1]  
    
1.  <span data-ttu-id="114b9-160">Просмотрите изменения на **вкладке "живые"**.  Текст `About Me` будет отображаться на странице.</span><span class="sxs-lookup"><span data-stu-id="114b9-160">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="114b9-161">Он больше, чем оставшаяся часть текста, так как `<h1>` элемент представляет заголовок раздела.</span><span class="sxs-lookup"><span data-stu-id="114b9-161">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="114b9-162">В веб-браузере стили заголовков автоматически заменяются на более крупные размеры шрифта.</span><span class="sxs-lookup"><span data-stu-id="114b9-162">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    > ##### <span data-ttu-id="114b9-163">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="114b9-163">Figure 7</span></span>  
    > <span data-ttu-id="114b9-164">Новый заголовок отображается на вкладке "живые"</span><span class="sxs-lookup"><span data-stu-id="114b9-164">The new heading is visible in the live tab</span></span>  
    > ![Новый заголовок отображается на вкладке "живые"][ImageHtmlAdd2]  
    
1.  <span data-ttu-id="114b9-166">Вернувшись на **вкладку Редактор**, вставьте `<p>I am learning HTML.  Recent accomplishments:</p>` строку под тем местом, где они просто размещены `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="114b9-166">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### <span data-ttu-id="114b9-167">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="114b9-167">Figure 8</span></span>  
    > <span data-ttu-id="114b9-168">На вкладке "редактор" выделена новая программа</span><span class="sxs-lookup"><span data-stu-id="114b9-168">The new code is highlighted in the editor tab</span></span>  
    > ![На вкладке "редактор" выделена новая программа][ImageHtmlAdd3]  
    
1.  <span data-ttu-id="114b9-170">Просмотрите изменения на **вкладке "живые"**.</span><span class="sxs-lookup"><span data-stu-id="114b9-170">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="114b9-171">Вернитесь на **вкладку Редактор**и добавьте список ваших достижений.</span><span class="sxs-lookup"><span data-stu-id="114b9-171">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="114b9-172">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="114b9-172">Figure 9</span></span>  
    > <span data-ttu-id="114b9-173">На вкладке "редактор" выделена новая программа</span><span class="sxs-lookup"><span data-stu-id="114b9-173">The new code is highlighted in the editor tab</span></span>  
    > ![На вкладке "редактор" выделена новая программа][ImageHtmlAdd4]  
    
1.  <span data-ttu-id="114b9-175">Опять же, вернитесь на **вкладку динамический** , чтобы убедиться, что новое содержимое отображается правильно.</span><span class="sxs-lookup"><span data-stu-id="114b9-175">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    > ##### <span data-ttu-id="114b9-176">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="114b9-176">Figure 10</span></span>  
    > <span data-ttu-id="114b9-177">Новый список отображается на вкладке "живые"</span><span class="sxs-lookup"><span data-stu-id="114b9-177">The new list is visible in the live tab</span></span>  
    > ![Новый список отображается на вкладке "живые"][ImageHtmlAdd5]  
    
## <span data-ttu-id="114b9-179">Поэкспериментировать с изменениями содержимого в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="114b9-179">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="114b9-180">Если вы разрабатываете большую страницу с большим количеством HTML-файлов, вы можете представить, что она может быть довольно утомительной, чтобы просматривать изменения, особенно если вы не уверены, что нужно сделать, чтобы они были размещены на странице.</span><span class="sxs-lookup"><span data-stu-id="114b9-180">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="114b9-181">Microsoft Edge DevTools поможет вам поэкспериментировать с изменениями содержимого, не выходя из вкладки Live.</span><span class="sxs-lookup"><span data-stu-id="114b9-181">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="114b9-182">Сведения о различиях между HTML и DOM</span><span class="sxs-lookup"><span data-stu-id="114b9-182">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="114b9-183">Перед тем как приступить к редактированию содержимого в Microsoft Edge DevTools, полезно понять разницу между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-183">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="114b9-184">Лучший способ освоить это можно, например:</span><span class="sxs-lookup"><span data-stu-id="114b9-184">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="114b9-185">Перейдите на **вкладку динамический**.  В нижней части страницы отображается текст `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="114b9-185">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    > ###### <span data-ttu-id="114b9-186">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="114b9-186">Figure 11</span></span>  
    > <span data-ttu-id="114b9-187">В нижней части страницы `A new element!?!` можно видеть текст</span><span class="sxs-lookup"><span data-stu-id="114b9-187">At the bottom of the page the text `A new element!?!` can be seen</span></span>  
    > ![В нижней части страницы текст — это новый элемент!?!][ImageHtmlDom1]  
    
1.  <span data-ttu-id="114b9-190">Вернитесь на **вкладку Редактор** и попробуйте найти этот текст в `index.html` .</span><span class="sxs-lookup"><span data-stu-id="114b9-190">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="114b9-191">Это не так!</span><span class="sxs-lookup"><span data-stu-id="114b9-191">It's not there!</span></span>  
    
    > ##### <span data-ttu-id="114b9-192">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="114b9-192">Figure 12</span></span>  
    > <span data-ttu-id="114b9-193">Текст загадкы `A new element!?!` не удается найти в</span><span class="sxs-lookup"><span data-stu-id="114b9-193">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    > ![Текст "Загадка" — новый элемент!?!][ImageHtmlDom2]  
    
1.  <span data-ttu-id="114b9-196">Вернитесь на **вкладку динамический**, щелкните правой кнопкой мыши `A new element!?!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="114b9-196">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="114b9-197">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="114b9-197">Figure 13</span></span>  
    > <span data-ttu-id="114b9-198">Проверка текста</span><span class="sxs-lookup"><span data-stu-id="114b9-198">Inspecting some text</span></span>  
    > ![Проверка текста][ImageHtmlDom3]  
    
    <span data-ttu-id="114b9-200">DevTools открывается вместе со страницей.</span><span class="sxs-lookup"><span data-stu-id="114b9-200">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="114b9-201">выделяется синим цветом.</span><span class="sxs-lookup"><span data-stu-id="114b9-201">is highlighted blue.</span></span>  <span data-ttu-id="114b9-202">Несмотря на то, что структура в DevTools выглядит так же, как и у вашего HTML-кода, она действительно является **деревом DOM**.</span><span class="sxs-lookup"><span data-stu-id="114b9-202">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    > ##### <span data-ttu-id="114b9-203">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="114b9-203">Figure 14</span></span>  
    > <span data-ttu-id="114b9-204">DevTools открывается вместе со страницей</span><span class="sxs-lookup"><span data-stu-id="114b9-204">DevTools is open alongside the page</span></span>  
    > ![DevTools открывается вместе со страницей][ImageHtmlDom4]  
    
<span data-ttu-id="114b9-206">При загрузке страницы браузер использует HTML для создания *начального* содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="114b9-206">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="114b9-207">Модель DOM представляет *Текущее* содержимое страницы, которое может изменяться с течением времени.</span><span class="sxs-lookup"><span data-stu-id="114b9-207">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="114b9-208">Содержимое Mysterious `<div>A new element!?!</div>` будет добавлено на страницу из `<script src="new.js"></script>` -за тега в нижней части HTML.</span><span class="sxs-lookup"><span data-stu-id="114b9-208">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="114b9-209">Этот тег вызывает выполнение кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="114b9-209">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="114b9-210">Более подробно о JavaScript можно узнать в более подробном учебнике, но теперь его можно рассматривать как язык программирования, который может изменить содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="114b9-210">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="114b9-211">В этом конкретном случае код JavaScript добавляется `<div>A new element!?!</div>` на страницу.</span><span class="sxs-lookup"><span data-stu-id="114b9-211">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="114b9-212">Причина в том, что этот загадкный текст отображается на живой странице, но не в HTML.</span><span class="sxs-lookup"><span data-stu-id="114b9-212">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="114b9-213">Редактирование модели DOM</span><span class="sxs-lookup"><span data-stu-id="114b9-213">Edit the DOM</span></span>   

<span data-ttu-id="114b9-214">Если вы хотите быстро поэкспериментировать с изменениями содержимого, не выходя из вкладки Live, попробуйте DevTools.</span><span class="sxs-lookup"><span data-stu-id="114b9-214">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="114b9-215">В DevTools щелкните правой кнопкой мыши `Your site!` и выберите команду **изменить в HTML**.</span><span class="sxs-lookup"><span data-stu-id="114b9-215">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  

    > ##### <span data-ttu-id="114b9-216">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="114b9-216">Figure 15</span></span>  
    > <span data-ttu-id="114b9-217">Редактирование узла в формате HTML</span><span class="sxs-lookup"><span data-stu-id="114b9-217">Editing the node as HTML</span></span>  
    > ![Редактирование узла в формате HTML][ImageHtmlEdit1]  
    
1.  <span data-ttu-id="114b9-219">Замените `<p>Your site!</p>` на код ниже.</span><span class="sxs-lookup"><span data-stu-id="114b9-219">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="114b9-220">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="114b9-220">Figure 16</span></span>  
    > <span data-ttu-id="114b9-221">Редактирование узла в формате HTML</span><span class="sxs-lookup"><span data-stu-id="114b9-221">Editing the node as HTML</span></span>  
    > ![Редактирование узла в формате HTML][ImageHtmlEdit2]  
    
1.  <span data-ttu-id="114b9-223">Нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения, или щелкните любое место за пределами поля.</span><span class="sxs-lookup"><span data-stu-id="114b9-223">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="114b9-224">Изменения автоматически отображаются в режиме реального времени на странице.</span><span class="sxs-lookup"><span data-stu-id="114b9-224">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="114b9-225">Текст `Your site!` заменен новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="114b9-225">The text `Your site!` has been replaced with the new content.</span></span>  
    
    > ##### <span data-ttu-id="114b9-226">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="114b9-226">Figure 17</span></span>  
    > <span data-ttu-id="114b9-227">Новое содержимое немедленно появляется на странице</span><span class="sxs-lookup"><span data-stu-id="114b9-227">The new content shows up immediately on the page</span></span>  
    > ![Новое содержимое немедленно появляется на странице][ImageHtmlEdit3]  
    
<span data-ttu-id="114b9-229">Этот рабочий процесс хорошо подходит только для экспериментов с изменениями контента.</span><span class="sxs-lookup"><span data-stu-id="114b9-229">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="114b9-230">Если вы перезагрузите страницу или закроете ее, ваши изменения будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="114b9-230">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="114b9-231">Если вы используете этот рабочий процесс и хотите сохранить изменения, вам потребуется вручную скопировать эти изменения на HTML-код.</span><span class="sxs-lookup"><span data-stu-id="114b9-231">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="114b9-232">В следующей паре разделов показаны другие способы изменения контента из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-232">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="114b9-233">Изменение порядка узлов</span><span class="sxs-lookup"><span data-stu-id="114b9-233">Reorder nodes</span></span>   

<span data-ttu-id="114b9-234">Вы также можете изменить порядок узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-234">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="114b9-235">Например, на веб-странице в нижней части окна находится меню навигации.</span><span class="sxs-lookup"><span data-stu-id="114b9-235">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="114b9-236">Чтобы переместить элемент в начало страницы, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="114b9-236">To move it to the top:</span></span>  

1.  <span data-ttu-id="114b9-237">Найдите `<nav>` узел в **дереве DOM** DevTools.</span><span class="sxs-lookup"><span data-stu-id="114b9-237">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="114b9-238">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="114b9-238">Figure 18</span></span>  
    > <span data-ttu-id="114b9-239">Узел навигации выделяется синим цветом в DevTools</span><span class="sxs-lookup"><span data-stu-id="114b9-239">The nav node is highlighted blue in DevTools</span></span>  
    > ![Узел навигации выделяется синим цветом в DevTools][ImageHtmlReorder1]  
    
1.  <span data-ttu-id="114b9-241">Перетащите `<nav>` узел в верхнюю части экрана, чтобы он был первым дочерним `<body>` узлом узла.</span><span class="sxs-lookup"><span data-stu-id="114b9-241">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    > ##### <span data-ttu-id="114b9-242">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="114b9-242">Figure 19</span></span>  
    > <span data-ttu-id="114b9-243">Перетаскивание узла навигации в начало</span><span class="sxs-lookup"><span data-stu-id="114b9-243">Dragging the nav node to the top</span></span>  
    > ![Перетаскивание узла навигации в начало][ImageHtmlReorder2]  
    
    <span data-ttu-id="114b9-245">`<nav>`Теперь узел отображается в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="114b9-245">The `<nav>` node is now displaying at the top of your page.</span></span>  
    
    > ##### <span data-ttu-id="114b9-246">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="114b9-246">Figure 20</span></span>  
    > <span data-ttu-id="114b9-247">Узел навигации находится в верхней части страницы</span><span class="sxs-lookup"><span data-stu-id="114b9-247">The nav node is at the top of the page</span></span>  
    > ![Узел навигации находится в верхней части страницы][ImageHtmlReorder3]  
    
### <span data-ttu-id="114b9-249">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="114b9-249">Delete a node</span></span>   

<span data-ttu-id="114b9-250">Вы также можете удалить узлы из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-250">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="114b9-251">В **дереве DOM**щелкните `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="114b9-251">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="114b9-252">DevTools выделяет узел синим цветом.</span><span class="sxs-lookup"><span data-stu-id="114b9-252">DevTools highlights the node blue.</span></span>  
    
    > ##### <span data-ttu-id="114b9-253">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="114b9-253">Figure 21</span></span>  
    > <span data-ttu-id="114b9-254">Выбор узла для удаления</span><span class="sxs-lookup"><span data-stu-id="114b9-254">Selecting the node to be deleted</span></span>  
    > ![Выбор узла для удаления][ImageHtmlDelete1]  
    
1.  <span data-ttu-id="114b9-256">Нажмите клавишу `Delete` на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="114b9-256">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="114b9-257">`<div>A new element!?!</div>`Узел удаляется из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-257">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="114b9-258">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="114b9-258">Figure 22</span></span>  
    > <span data-ttu-id="114b9-259">Узел удален</span><span class="sxs-lookup"><span data-stu-id="114b9-259">The node has been deleted</span></span>  
    > ![Узел удален][ImageHtmlDelete2]  
    
## <span data-ttu-id="114b9-261">Копирование изменений</span><span class="sxs-lookup"><span data-stu-id="114b9-261">Copy your changes</span></span>   

<span data-ttu-id="114b9-262">Почти все готово.</span><span class="sxs-lookup"><span data-stu-id="114b9-262">You're almost done.</span></span>  <span data-ttu-id="114b9-263">Вы внесли несколько изменений на странице в DevTools, но они еще не сохранились в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="114b9-263">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="114b9-264">Обновите **вкладку Live**.  Изменения, внесенные в дереве DOM, исчезнут.</span><span class="sxs-lookup"><span data-stu-id="114b9-264">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="114b9-265">В частности, текст `Your site!` возвращается в верхней части страницы, а текст `A new element!?!` возвращается в нижнюю часть.</span><span class="sxs-lookup"><span data-stu-id="114b9-265">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    > ##### <span data-ttu-id="114b9-266">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="114b9-266">Figure 23</span></span>  
    > <span data-ttu-id="114b9-267">Внесенные вами изменения исчезли</span><span class="sxs-lookup"><span data-stu-id="114b9-267">The changes that you've made are gone</span></span>  
    > ![Внесенные вами изменения исчезли][ImageHtmlCopy1]  

1.  <span data-ttu-id="114b9-269">Скопируйте приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="114b9-269">Copy the code below.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  <span data-ttu-id="114b9-270">Вернитесь на **вкладку Редактор** и замените содержимое `index.html` файла кодом, который вы только что скопировали.</span><span class="sxs-lookup"><span data-stu-id="114b9-270">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    > ##### <span data-ttu-id="114b9-271">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="114b9-271">Figure 24</span></span>  
    > <span data-ttu-id="114b9-272">Как `index.html` должен выглядеть файл</span><span class="sxs-lookup"><span data-stu-id="114b9-272">How your `index.html` file should look</span></span>  
    > ![Как должен выглядеть файл index. HTML][ImageHtmlCopy2]  
    
## <span data-ttu-id="114b9-274">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="114b9-274">Next steps</span></span>   

*   <span data-ttu-id="114b9-275">Чтобы узнать, как изменить стиль страницы и поэкспериментировать с изменениями стиля в Microsoft Edge DevTools, выполните следующие шаги в этой серии. Приступая к [работе с CSS][DevToolsBeginnersCss].</span><span class="sxs-lookup"><span data-stu-id="114b9-275">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="114b9-276">Ознакомьтесь [с введением в DOM][MDNIntroductionDom] , чтобы узнать больше об DOM.</span><span class="sxs-lookup"><span data-stu-id="114b9-276">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="114b9-277">Ознакомьтесь с курсом, например [Знакомство с веб-разработкой][CourseraIntroductionToWebDevelopment] , чтобы получить больше возможностей для веб-разработки.</span><span class="sxs-lookup"><span data-stu-id="114b9-277">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Рисунок 1: готовый веб-сайт"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Рисунок 2: вкладка "редактор""  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Рисунок 3: меню "Параметры проекта""  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Рисунок 4: смешанный проект"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Рисунок 5. Вкладка "динамический""  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Рисунок 6: на вкладке "редактор" выделена новая программа"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Рисунок 7: новый заголовок отображается на вкладке "живые""  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Рисунок 8: на вкладке "редактор" выделена новая программа"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "На рисунке 9: на вкладке "редактор" выделена кнопка "создать код"."  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Рисунок 10: новый список отображается на вкладке "живые""  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "На рисунке 11: в нижней части страницы текст — это новый элемент!?! может отображаться"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Рисунок 12: текст "Загадка" — новый элемент!?! не удается найти в index. HTML"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Рисунок 13: проверка текста"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Рисунок 14: DevTools открывается вместе со страницей"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Рисунок 15: Редактирование узла в формате HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Рисунок 16: Редактирование узла в формате HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Рисунок 17: новое содержимое немедленно появляется на странице"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Рисунок 18: узел навигации выделен синим цветом в DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "На рисунке 19 показано, как перетащить узел навигации в начало."  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Рисунок 20: узел навигации находится в верхней части страницы."  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Рисунок 21: Выбор узла для удаления"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Рис. 22: узел удален"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Рис. 23: изменения, внесенные вами, исчезли"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Рисунок 24: внешний вид файла index. HTML"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools для начинающих: Приступая к работе с CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Общие сведения о веб-разработке | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index. HTML-alluring-удар | Цепь"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Начало работы с HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="114b9-308">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="114b9-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="114b9-309">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/html) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="114b9-309">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="114b9-311">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="114b9-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  

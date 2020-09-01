---
title: 'DevTools для начинающих: Приступая к работе с HTML и моделью DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 50dfd8595c270a2532f55b71307b42c3636bba3c
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983078"
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

# <span data-ttu-id="6cc0e-103">DevTools для начинающих: Приступая к работе с HTML и моделью DOM</span><span class="sxs-lookup"><span data-stu-id="6cc0e-103">DevTools for beginners: Get started with HTML and the DOM</span></span>   

<span data-ttu-id="6cc0e-104">Это первый из ряда учебников, в котором изучаются основы разработки веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="6cc0e-105">Кроме того, вы узнаете о наборе средств для веб-разработчиков, именуемых Microsoft Edge DevTools, которые могут повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="6cc0e-106">В этом конкретном учебнике вы узнаете о HTML и модели DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="6cc0e-107">HTML — это одна из основных методик разработки веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="6cc0e-108">Это язык, управляющий структурой и содержимым веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="6cc0e-109">Модель DOM также связана со структурой и контентом веб-страниц, но вы узнаете об этом позже.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="6cc0e-110">Цели</span><span class="sxs-lookup"><span data-stu-id="6cc0e-110">Goals</span></span>   

<span data-ttu-id="6cc0e-111">Вы собираетесь познакомиться с веб-разработкой, завершив создание собственного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="6cc0e-112">По мере того, как вы закончите все учебные курсы в серии *DevTools для начинающих* , ваш готовый сайт будет выглядеть так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like in the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="6cc0e-114">Готовый сайт</span><span class="sxs-lookup"><span data-stu-id="6cc0e-114">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="6cc0e-115">В конце этого учебника вы узнаете:</span><span class="sxs-lookup"><span data-stu-id="6cc0e-115">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="6cc0e-116">Как HTML и DOM создают содержимое, которое отображается на веб-страницах.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-116">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="6cc0e-117">Как Microsoft Edge DevTools помогает экспериментировать с изменениями HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-117">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="6cc0e-118">Разница между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-118">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="6cc0e-119">У тебя также есть реальный веб-сайт!</span><span class="sxs-lookup"><span data-stu-id="6cc0e-119">You'll also have a real website!</span></span>  <span data-ttu-id="6cc0e-120">Вы можете использовать этот сайт для размещения резюме или блога.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-120">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="6cc0e-121">Что вам понадобится</span><span class="sxs-lookup"><span data-stu-id="6cc0e-121">Prerequisites</span></span>   

<span data-ttu-id="6cc0e-122">Прежде чем приступить к работе с учебником, выполните следующие требования:</span><span class="sxs-lookup"><span data-stu-id="6cc0e-122">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="6cc0e-123">Если вы не знакомы с форматом HTML, ознакомьтесь с разделом начало [работы с HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="6cc0e-123">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="6cc0e-124">Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="6cc0e-124">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="6cc0e-125">В этом учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-125">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="6cc0e-126">Настройка кода</span><span class="sxs-lookup"><span data-stu-id="6cc0e-126">Set up your code</span></span>   

<span data-ttu-id="6cc0e-127">Вы собираетесь создать сайт в редакторе кода на веб-сайте с именем "сбой".</span><span class="sxs-lookup"><span data-stu-id="6cc0e-127">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="6cc0e-128">Откройте [Исходный код][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="6cc0e-128">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="6cc0e-129">Эта вкладка будет называться **вкладкой "редактор"** в рамках этого учебника.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-129">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Вкладка "редактор"" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="6cc0e-131">Вкладка "редактор"</span><span class="sxs-lookup"><span data-stu-id="6cc0e-131">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-132">Щелкните **alluring-удар**.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-132">Click **alluring-shock**.</span></span>  <span data-ttu-id="6cc0e-133">В левом верхнем углу откроется меню "Параметры проекта".</span><span class="sxs-lookup"><span data-stu-id="6cc0e-133">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Меню "Параметры проекта"" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="6cc0e-135">Меню "Параметры проекта"</span><span class="sxs-lookup"><span data-stu-id="6cc0e-135">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-136">Щелкните **Remix Project (проект**).</span><span class="sxs-lookup"><span data-stu-id="6cc0e-136">Click **Remix Project**.</span></span>  <span data-ttu-id="6cc0e-137">При возникновении недостаточной версии создается копия проекта, которую можно редактировать и случайным образом создает новое имя для проекта.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-137">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="6cc0e-138">Содержимое будет таким же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-138">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Смешанный проект" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="6cc0e-140">Смешанный проект</span><span class="sxs-lookup"><span data-stu-id="6cc0e-140">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-141">Если вы планируете выполнить следующий учебник в этой серии, нажмите **Вход** и войдите в систему, чтобы завершить работу с учетной записью GitHub или Facebook.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-141">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="6cc0e-142">Если вы не входите в свою учетную запись, то после закрытия вкладки Правка вы потеряли возможность изменить этот проект.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-142">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="6cc0e-143">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-143">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="6cc0e-144">Откроется новая вкладка, на которой отображается активная страница.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-144">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="6cc0e-145">Эта вкладка будет называться на **вкладке динамический** в рамках этого учебника.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-145">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Вкладка "динамический"" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="6cc0e-147">Вкладка "динамический"</span><span class="sxs-lookup"><span data-stu-id="6cc0e-147">The live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6cc0e-148">Добавление содержимого</span><span class="sxs-lookup"><span data-stu-id="6cc0e-148">Add content</span></span>   

<span data-ttu-id="6cc0e-149">Ваш сайт совершенно пуст.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-149">Your site is pretty empty.</span></span>  <span data-ttu-id="6cc0e-150">Чтобы добавить содержимое, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-150">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="6cc0e-151">На **вкладке "редактор"** замените `<!-- You're "About Me" will go here.  -->` на `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="6cc0e-151">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="На вкладке "редактор" выделена новая программа" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="6cc0e-153">На вкладке "редактор" выделена новая программа</span><span class="sxs-lookup"><span data-stu-id="6cc0e-153">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="6cc0e-154">Просмотрите изменения на **вкладке "живые"**.  Текст `About Me` будет отображаться на странице.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-154">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="6cc0e-155">Он больше, чем оставшаяся часть текста, так как `<h1>` элемент представляет заголовок раздела.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-155">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="6cc0e-156">В веб-браузере стили заголовков автоматически заменяются на более крупные размеры шрифта.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-156">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Новый заголовок отображается на вкладке "живые"" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="6cc0e-158">Новый заголовок отображается на вкладке "живые"</span><span class="sxs-lookup"><span data-stu-id="6cc0e-158">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-159">Вернувшись на **вкладку Редактор**, вставьте `<p>I am learning HTML.  Recent accomplishments:</p>` строку под тем местом, где они просто размещены `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="6cc0e-159">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="На вкладке "редактор" выделена новая программа" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="6cc0e-161">На вкладке "редактор" выделена новая программа</span><span class="sxs-lookup"><span data-stu-id="6cc0e-161">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="6cc0e-162">Просмотрите изменения на **вкладке "живые"**.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-162">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="6cc0e-163">Вернитесь на **вкладку Редактор**и добавьте список ваших достижений.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-163">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="На вкладке "редактор" выделена новая программа" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="6cc0e-165">На вкладке "редактор" выделена новая программа</span><span class="sxs-lookup"><span data-stu-id="6cc0e-165">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="6cc0e-166">Опять же, вернитесь на **вкладку динамический** , чтобы убедиться, что новое содержимое отображается правильно.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-166">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Новый список отображается на вкладке "живые"" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="6cc0e-168">Новый список отображается на вкладке "живые"</span><span class="sxs-lookup"><span data-stu-id="6cc0e-168">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6cc0e-169">Поэкспериментировать с изменениями содержимого в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6cc0e-169">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="6cc0e-170">Если вы разрабатываете большую страницу с большим количеством HTML-файлов, вы можете представить, что она может быть довольно утомительной, чтобы просматривать изменения, особенно если вы не уверены, что нужно сделать, чтобы они были размещены на странице.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-170">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="6cc0e-171">Microsoft Edge DevTools поможет вам поэкспериментировать с изменениями содержимого, не выходя из вкладки Live.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-171">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="6cc0e-172">Сведения о различиях между HTML и DOM</span><span class="sxs-lookup"><span data-stu-id="6cc0e-172">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="6cc0e-173">Перед тем как приступить к редактированию содержимого в Microsoft Edge DevTools, полезно понять разницу между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-173">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="6cc0e-174">Лучший способ освоить это можно, например:</span><span class="sxs-lookup"><span data-stu-id="6cc0e-174">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="6cc0e-175">Перейдите на **вкладку динамический**.  В нижней части страницы отображается текст `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="6cc0e-175">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="В нижней части страницы текст — это новый элемент!?! может отображаться" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="6cc0e-178">В нижней части страницы текст — это новый элемент!?!</span><span class="sxs-lookup"><span data-stu-id="6cc0e-178">At the bottom of the page the text A new element!?!</span></span> <span data-ttu-id="6cc0e-179">может отображаться</span><span class="sxs-lookup"><span data-stu-id="6cc0e-179">can be seen</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-180">Вернитесь на **вкладку Редактор** и попробуйте найти этот текст в `index.html` .</span><span class="sxs-lookup"><span data-stu-id="6cc0e-180">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="6cc0e-181">Это не так!</span><span class="sxs-lookup"><span data-stu-id="6cc0e-181">It's not there!</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Текст "Загадка" — новый элемент!?! <span data-ttu-id="6cc0e-183">не удается найти в index.html</span><span class="sxs-lookup"><span data-stu-id="6cc0e-183">is nowhere to be found in index.html</span></span>" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="6cc0e-184">Текст загадкы `A new element!?!` не удается найти в</span><span class="sxs-lookup"><span data-stu-id="6cc0e-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-185">Вернитесь на **вкладку динамический**, щелкните правой кнопкой мыши `A new element!?!` и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-185">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Проверка текста" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="6cc0e-187">Проверка текста</span><span class="sxs-lookup"><span data-stu-id="6cc0e-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="6cc0e-188">DevTools открывается вместе со страницей.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="6cc0e-189">выделяется синим цветом.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-189">is highlighted blue.</span></span>  <span data-ttu-id="6cc0e-190">Несмотря на то, что структура в DevTools выглядит так же, как и у вашего HTML-кода, она действительно является **деревом DOM**.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools открывается вместе со страницей" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="6cc0e-192">DevTools открывается вместе со страницей</span><span class="sxs-lookup"><span data-stu-id="6cc0e-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6cc0e-193">При загрузке страницы браузер использует HTML для создания *начального* содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="6cc0e-194">Модель DOM представляет *Текущее* содержимое страницы, которое может изменяться с течением времени.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-194">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="6cc0e-195">Содержимое Mysterious `<div>A new element!?!</div>` будет добавлено на страницу из `<script src="new.js"></script>` -за тега в нижней части HTML.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="6cc0e-196">Этот тег вызывает выполнение кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="6cc0e-197">Более подробно о JavaScript можно узнать в более подробном учебнике, но теперь его можно рассматривать как язык программирования, который может изменить содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-197">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="6cc0e-198">В этом конкретном случае код JavaScript добавляется `<div>A new element!?!</div>` на страницу.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="6cc0e-199">Причина в том, что этот загадкный текст отображается на живой странице, но не в HTML.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="6cc0e-200">Редактирование модели DOM</span><span class="sxs-lookup"><span data-stu-id="6cc0e-200">Edit the DOM</span></span>   

<span data-ttu-id="6cc0e-201">Если вы хотите быстро поэкспериментировать с изменениями содержимого, не выходя из вкладки Live, попробуйте DevTools.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="6cc0e-202">В DevTools щелкните правой кнопкой мыши `Your site!` и выберите команду **изменить в HTML**.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-202">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Редактирование узла в формате HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="6cc0e-204">Редактирование узла в формате HTML</span><span class="sxs-lookup"><span data-stu-id="6cc0e-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-205">Замените `<p>Your site!</p>` на код ниже.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Редактирование узла в формате HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="6cc0e-207">Редактирование узла в формате HTML</span><span class="sxs-lookup"><span data-stu-id="6cc0e-207">Editing the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="6cc0e-208">Нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения, или щелкните любое место за пределами поля.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-208">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="6cc0e-209">Изменения автоматически отображаются в режиме реального времени на странице.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="6cc0e-210">Текст `Your site!` заменен новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Новое содержимое немедленно появляется на странице" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="6cc0e-212">Новое содержимое немедленно появляется на странице</span><span class="sxs-lookup"><span data-stu-id="6cc0e-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6cc0e-213">Этот рабочий процесс хорошо подходит только для экспериментов с изменениями контента.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="6cc0e-214">Если вы перезагрузите страницу или закроете ее, ваши изменения будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-214">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="6cc0e-215">Если вы используете этот рабочий процесс и хотите сохранить изменения, вам потребуется вручную скопировать эти изменения на HTML-код.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="6cc0e-216">В следующей паре разделов показаны другие способы изменения контента из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-216">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="6cc0e-217">Изменение порядка узлов</span><span class="sxs-lookup"><span data-stu-id="6cc0e-217">Reorder nodes</span></span>   

<span data-ttu-id="6cc0e-218">Вы также можете изменить порядок узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-218">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="6cc0e-219">Например, на веб-странице в нижней части окна находится меню навигации.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="6cc0e-220">Чтобы переместить элемент в начало страницы, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="6cc0e-221">Найдите `<nav>` узел в **дереве DOM** DevTools.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Узел навигации выделяется синим цветом в DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="6cc0e-223">Узел навигации выделяется синим цветом в DevTools</span><span class="sxs-lookup"><span data-stu-id="6cc0e-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-224">Перетащите `<nav>` узел в верхнюю части экрана, чтобы он был первым дочерним `<body>` узлом узла.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-224">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Перетаскивание узла навигации в начало" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="6cc0e-226">Перетаскивание узла навигации в начало</span><span class="sxs-lookup"><span data-stu-id="6cc0e-226">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="6cc0e-227">`<nav>`Теперь узел отображается в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-227">The `<nav>` node is now displaying at the top of your page.</span></span>  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Узел навигации находится в верхней части страницы" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="6cc0e-229">Узел навигации находится в верхней части страницы</span><span class="sxs-lookup"><span data-stu-id="6cc0e-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <span data-ttu-id="6cc0e-230">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="6cc0e-230">Delete a node</span></span>   

<span data-ttu-id="6cc0e-231">Вы также можете удалить узлы из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-231">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="6cc0e-232">В **дереве DOM**щелкните `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="6cc0e-232">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="6cc0e-233">DevTools выделяет узел синим цветом.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Выбор узла для удаления" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="6cc0e-235">Выбор узла для удаления</span><span class="sxs-lookup"><span data-stu-id="6cc0e-235">Selecting the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-236">Нажмите клавишу `Delete` на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-236">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="6cc0e-237">`<div>A new element!?!</div>`Узел удаляется из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Узел удален" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="6cc0e-239">Узел удален</span><span class="sxs-lookup"><span data-stu-id="6cc0e-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6cc0e-240">Копирование изменений</span><span class="sxs-lookup"><span data-stu-id="6cc0e-240">Copy your changes</span></span>   

<span data-ttu-id="6cc0e-241">Почти все готово.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-241">You're almost done.</span></span>  <span data-ttu-id="6cc0e-242">Вы внесли несколько изменений на странице в DevTools, но они еще не сохранились в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="6cc0e-243">Обновите **вкладку Live**.  Изменения, внесенные в дереве DOM, исчезнут.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="6cc0e-244">В частности, текст `Your site!` возвращается в верхней части страницы, а текст `A new element!?!` возвращается в нижнюю часть.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Внесенные вами изменения исчезли" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="6cc0e-246">Внесенные вами изменения исчезли</span><span class="sxs-lookup"><span data-stu-id="6cc0e-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6cc0e-247">Скопируйте приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-247">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="6cc0e-248">Вернитесь на **вкладку Редактор** и замените содержимое `index.html` файла кодом, который вы только что скопировали.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Как должен выглядеть файл index.html" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="6cc0e-250">Как `index.html` должен выглядеть файл</span><span class="sxs-lookup"><span data-stu-id="6cc0e-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6cc0e-251">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6cc0e-251">Next steps</span></span>   

*   <span data-ttu-id="6cc0e-252">Чтобы узнать, как изменить стиль страницы и поэкспериментировать с изменениями стиля в Microsoft Edge DevTools, выполните следующие шаги в этой серии. Приступая к [работе с CSS][DevToolsBeginnersCss].</span><span class="sxs-lookup"><span data-stu-id="6cc0e-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="6cc0e-253">Ознакомьтесь [с введением в DOM][MDNIntroductionDom] , чтобы узнать больше об DOM.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="6cc0e-254">Ознакомьтесь с курсом, например [Знакомство с веб-разработкой][CourseraIntroductionToWebDevelopment] , чтобы получить больше возможностей для веб-разработки.</span><span class="sxs-lookup"><span data-stu-id="6cc0e-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools для начинающих: Приступая к работе с CSS | Документы Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Общие сведения о веб-разработке | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring-удар | Цепь"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Начало работы с HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="6cc0e-261">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6cc0e-261">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6cc0e-262">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/html) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="6cc0e-262">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6cc0e-264">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6cc0e-264">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  

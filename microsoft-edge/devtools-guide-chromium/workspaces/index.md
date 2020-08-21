---
title: Редактирование файлов с помощью рабочих областей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8a31dd9fbfe492cf8eaacc654f7d501925f730f2
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942180"
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

# <span data-ttu-id="f5607-103">Редактирование файлов с помощью рабочих областей</span><span class="sxs-lookup"><span data-stu-id="f5607-103">Edit files with Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="f5607-104">Цель этого учебника — предоставить на практические практические задачи по настройке и использованию рабочих областей, чтобы вы сможете использовать рабочие области в собственных проектах.</span><span class="sxs-lookup"><span data-stu-id="f5607-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="f5607-105">Вы можете сохранить изменения в исходном коде на локальном компьютере, которые были сделаны в DevTools после включения рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="f5607-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f5607-106">**Предварительные предварительные проверки:** прежде чем приступать к учебнику, необходимо узнать, как выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f5607-106">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="f5607-107">Создание веб-страниц с помощью html, CSS и JavaScript</span><span class="sxs-lookup"><span data-stu-id="f5607-107">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="f5607-108">Внесение основных изменений в CSS с помощью Средств разработки</span><span class="sxs-lookup"><span data-stu-id="f5607-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="f5607-109">Запуск локального HTTP-сервера</span><span class="sxs-lookup"><span data-stu-id="f5607-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="f5607-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="f5607-110">Overview</span></span>  

<span data-ttu-id="f5607-111">Рабочие области дают возможность сохранить изменения, внесенные в Devtools, в локальную копию файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f5607-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="f5607-112">В этом учебнике у вас должны быть следующие параметры компьютера:</span><span class="sxs-lookup"><span data-stu-id="f5607-112">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="f5607-113">У вас есть исходный код сайта на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="f5607-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="f5607-114">Вы запускаете локальный веб-сервер из исходного каталога кодов, чтобы сайт был доступен самого `localhost:8080` языка.</span><span class="sxs-lookup"><span data-stu-id="f5607-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="f5607-115">Вы открывали `localhost:8080` в Microsoft Edge и используете средства разработчиков для изменения CSS-сайта.</span><span class="sxs-lookup"><span data-stu-id="f5607-115">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="f5607-116">Если включена поддержка рабочих областей, изменения, внесенные в DevTools, сохраняются в исходном коде на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="f5607-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="f5607-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="f5607-117">Limitations</span></span>  

<span data-ttu-id="f5607-118">Если вы используете современной структуру, вероятно, исходный код из формата, который проще сохранять в формат, оптимизированный для работы как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="f5607-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="f5607-119">Обычно рабочие области можно сопоставить оптимизированный код с исходным кодом с помощью исходных [карт.][TreehouseBlogSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="f5607-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="f5607-120">Однако между структурами используется множество вариантов, которые используются в каждой из них.</span><span class="sxs-lookup"><span data-stu-id="f5607-120">But there is a lot of variation between frameworks over how each uses source maps.</span></span>  <span data-ttu-id="f5607-121">Дисперсии просто поддерживают все варианты.</span><span class="sxs-lookup"><span data-stu-id="f5607-121">Devtools simply does support all of the variations.</span></span>  

<span data-ttu-id="f5607-122">Рабочие области не совместимо с приведенной ниже таблицей.</span><span class="sxs-lookup"><span data-stu-id="f5607-122">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="f5607-123">Создать редактироваемое приложение</span><span class="sxs-lookup"><span data-stu-id="f5607-123">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <span data-ttu-id="f5607-124">Дополнительные функции: локальные переопределения</span><span class="sxs-lookup"><span data-stu-id="f5607-124">Related feature: Local overrides</span></span>  

<span data-ttu-id="f5607-125">**Локальный переопределение —** это еще один компонент DevTools, аналогичная рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f5607-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="f5607-126">Используйте локальные переопределения, если вы хотите экспертировать с изменениями на странице и вам нужно просматривать изменения на странице, но не беспокойтесь об изменениях исходного кода страницы.</span><span class="sxs-lookup"><span data-stu-id="f5607-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see the changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="f5607-127">Шаг 1. Настройка</span><span class="sxs-lookup"><span data-stu-id="f5607-127">Step 1: Set up</span></span>  

<span data-ttu-id="f5607-128">Выполните указанные ниже действия, чтобы повысить эффективность работы с рабочими областями.</span><span class="sxs-lookup"><span data-stu-id="f5607-128">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="f5607-129">Настройка демонстрации</span><span class="sxs-lookup"><span data-stu-id="f5607-129">Set up the demo</span></span>  

1.  <span data-ttu-id="f5607-130">[Открыть демонстрацию.][GlitchWorkspacesDemo]</span><span class="sxs-lookup"><span data-stu-id="f5607-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Проект в glitch-проекте" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="f5607-132">Проект в glitch-проекте</span><span class="sxs-lookup"><span data-stu-id="f5607-132">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="f5607-133">Создайте каталог `app` на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f5607-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="f5607-134">Сохраняйте копии файлов из `workspaces-demo` каталога в `app` каталог.</span><span class="sxs-lookup"><span data-stu-id="f5607-134">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="f5607-135">Для остального учебника каталог называется `~/Desktop/app` каталогом.</span><span class="sxs-lookup"><span data-stu-id="f5607-135">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="f5607-136">Запустите локальный веб-сервер `~/Desktop/app` в.</span><span class="sxs-lookup"><span data-stu-id="f5607-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="f5607-137">Ниже приведен пример кода для запуска, но вы можете использовать то, что `SimpleHTTPServer` вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="f5607-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f5607-138">Откройте вкладку в Microsoft Edge и перейдите к версии сайта, размещенной локально.</span><span class="sxs-lookup"><span data-stu-id="f5607-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="f5607-139">Вы должны иметь доступ по URL-адресу, такому `localhost:8080` как. `http://0.0.0.0:8080`</span><span class="sxs-lookup"><span data-stu-id="f5607-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="f5607-140">Точный [номер порта][WikiPortURLs] может быть другим.</span><span class="sxs-lookup"><span data-stu-id="f5607-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Демонстрация" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="f5607-142">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="f5607-142">The demo</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="f5607-143">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="f5607-143">Set up DevTools</span></span>  

1.  <span data-ttu-id="f5607-144">Выберите `Control` + `Shift` + `J` \(Windows\) `Command` + `Option` + `J` или \(macOS\), чтобы открыть **панель консоли** devTools.</span><span class="sxs-lookup"><span data-stu-id="f5607-144">Select `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Панель консоли" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="f5607-146">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="f5607-146">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f5607-147">Откройте **вкладку "Источники".**</span><span class="sxs-lookup"><span data-stu-id="f5607-147">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="f5607-148">Откройте **вкладку Filesystem.**</span><span class="sxs-lookup"><span data-stu-id="f5607-148">Choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Вкладка "Файловая система"" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="f5607-150">Вкладка **"Файловая система"**</span><span class="sxs-lookup"><span data-stu-id="f5607-150">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f5607-151">Выберите **команду "Добавить папку в рабочую область".**</span><span class="sxs-lookup"><span data-stu-id="f5607-151">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="f5607-152">Введите `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="f5607-152">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="f5607-153">Выберите **"Разрешить",** чтобы предоставить devTools разрешение на чтение и запись в каталог.</span><span class="sxs-lookup"><span data-stu-id="f5607-153">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="f5607-154">На **вкладке "Файлная** система" рядом с ней появится зеленая `index.html` `script.js` пунктирная линия, а также зеленая `styles.css` пунктирная линия.</span><span class="sxs-lookup"><span data-stu-id="f5607-154">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="f5607-155">Эти зеленые точки означали, что DevTools установил сопоставленное сопоставленное сопоставление между сетевыми ресурсами страницы и `~/Desktop/app` файлами.</span><span class="sxs-lookup"><span data-stu-id="f5607-155">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="На вкладке "Файлная система" отображается сопоставление между локальными файлами и сетью" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="f5607-157">На **вкладке "Файлная** система" отображается сопоставление между локальными файлами и сетью</span><span class="sxs-lookup"><span data-stu-id="f5607-157">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f5607-158">Шаг 2. Сохранение изменения CSS на диск</span><span class="sxs-lookup"><span data-stu-id="f5607-158">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="f5607-159">`styles.css`Откройте.</span><span class="sxs-lookup"><span data-stu-id="f5607-159">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f5607-160">Для `color` свойства `h1` элементов задано значение `fuchsia` ..</span><span class="sxs-lookup"><span data-stu-id="f5607-160">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Просмотр стилей.css в текстовом редакторе" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="f5607-162">Просмотр `styles.css` в текстовом редакторе</span><span class="sxs-lookup"><span data-stu-id="f5607-162">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f5607-163">Откройте **вкладку "Элементы".**</span><span class="sxs-lookup"><span data-stu-id="f5607-163">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="f5607-164">Измените значение `color` свойства `<h1>` элемента на избранный цвет.</span><span class="sxs-lookup"><span data-stu-id="f5607-164">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="f5607-165">Помните, что чтобы правила CSS применены к этому представлению, необходимо выбрать элемент в дереве DOM, чтобы отобразить примененные к нему правила `<h1>` CSS в **области "Стили".** **DOM Tree**</span><span class="sxs-lookup"><span data-stu-id="f5607-165">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="f5607-166">Зеленая точка рядом с значками, с которыми `styles.css:1` вы вносите `~/Desktop/app/styles.css` изменения.</span><span class="sxs-lookup"><span data-stu-id="f5607-166">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Зеленый индикатор связывания файла" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="f5607-168">Зеленый индикатор связывания файла</span><span class="sxs-lookup"><span data-stu-id="f5607-168">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f5607-169">Снова `styles.css` откройте его в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="f5607-169">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="f5607-170">Теперь `color` для свойства будет настроен ваш избранный цвет.</span><span class="sxs-lookup"><span data-stu-id="f5607-170">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="f5607-171">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="f5607-171">Refresh the page.</span></span>  <span data-ttu-id="f5607-172">Цвет элемента `<h1>` по-прежнему имеет избранный цвет.</span><span class="sxs-lookup"><span data-stu-id="f5607-172">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="f5607-173">Изменения остаются в обновлении, так как при внесении изменений средств разработчиков сохраняются изменения, сохраненные на диск.</span><span class="sxs-lookup"><span data-stu-id="f5607-173">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="f5607-174">После этого при обновлении страницы измененная копия файла с диска.</span><span class="sxs-lookup"><span data-stu-id="f5607-174">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <span data-ttu-id="f5607-175">Шаг 3. Сохранение изменения В ФОРМАТе HTML на диск</span><span class="sxs-lookup"><span data-stu-id="f5607-175">Step 3: Save an HTML change to disk</span></span>  

### <span data-ttu-id="f5607-176">Изменение HTML-кода из панели элементов</span><span class="sxs-lookup"><span data-stu-id="f5607-176">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="f5607-177">Html можно вносить изменения в html-файл из панели элементов, но изменения в дереве DOM не сохраняются на диске и влияют только на текущий сеанс браузера.</span><span class="sxs-lookup"><span data-stu-id="f5607-177">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="f5607-178">Дерево DOM не является html.</span><span class="sxs-lookup"><span data-stu-id="f5607-178">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** panel  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <span data-ttu-id="f5607-179">Изменение HTML-кода из панели "Источники"</span><span class="sxs-lookup"><span data-stu-id="f5607-179">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="f5607-180">Если вы хотите сохранить изменение на HTML-адресстраницы, сделайте это с **помощью панели "Источники".**</span><span class="sxs-lookup"><span data-stu-id="f5607-180">If you want to save a change to the html of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="f5607-181">Откройте **вкладку "Источники".**</span><span class="sxs-lookup"><span data-stu-id="f5607-181">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="f5607-182">Выберите **вкладку Страницы.**</span><span class="sxs-lookup"><span data-stu-id="f5607-182">Choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="f5607-183">Выберите **(индекс).**</span><span class="sxs-lookup"><span data-stu-id="f5607-183">Choose **(index)**.</span></span>  <span data-ttu-id="f5607-184">Откроется HTML-код страницы.</span><span class="sxs-lookup"><span data-stu-id="f5607-184">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="f5607-185">Замените `<h1>Workspaces Demo</h1>` `<h1>I ❤️  Cake</h1>` их.</span><span class="sxs-lookup"><span data-stu-id="f5607-185">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="f5607-186">См. на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="f5607-186">See the following figure.</span></span>  
1.  <span data-ttu-id="f5607-187">Выберите `Control` + `S` \(Windows\) `Command` + `S` или \(macOS\), чтобы сохранить изменение.</span><span class="sxs-lookup"><span data-stu-id="f5607-187">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="f5607-188">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="f5607-188">Refresh the page.</span></span>  <span data-ttu-id="f5607-189">Элемент `<h1>` по-прежнему отображает новый текст.</span><span class="sxs-lookup"><span data-stu-id="f5607-189">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Изменение HTML-кода из панели "Источники"" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="f5607-191">Изменение HTML-кода **из панели "Источники"**</span><span class="sxs-lookup"><span data-stu-id="f5607-191">Change HTML from the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f5607-192">`~/Desktop/app/index.html`Откройте.</span><span class="sxs-lookup"><span data-stu-id="f5607-192">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="f5607-193">Элемент `<h1>` содержит новый текст.</span><span class="sxs-lookup"><span data-stu-id="f5607-193">The `<h1>` element contains the new text.</span></span>  
    
## <span data-ttu-id="f5607-194">Шаг 4. Сохранение изменения JavaScript на диск</span><span class="sxs-lookup"><span data-stu-id="f5607-194">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="f5607-195">В **области "Источники"** также можно вносить изменения в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f5607-195">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="f5607-196">Но иногда при внесении изменений на сайт необходимо получить доступ к другим панелям, таким как панель "Элементы" или "Консоль", и при внесении изменений на сайт. **Elements** **Console**</span><span class="sxs-lookup"><span data-stu-id="f5607-196">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="f5607-197">Существует способ открыть **панель "Источники"** рядом с другими панелями.</span><span class="sxs-lookup"><span data-stu-id="f5607-197">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="f5607-198">Откройте **вкладку "Элементы".**</span><span class="sxs-lookup"><span data-stu-id="f5607-198">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="f5607-199">Выберите `Control` + `Shift` + `P` \(Windows\) `Command` + `Shift` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="f5607-199">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="f5607-200">Откроется **меню** команд.</span><span class="sxs-lookup"><span data-stu-id="f5607-200">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="f5607-201">Введите `QS` текст, а затем выберите **"Показать экспресс-источник".**</span><span class="sxs-lookup"><span data-stu-id="f5607-201">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="f5607-202">В нижней части окна DevTools теперь находится вкладка **"Быстрый источник".**  Вкладка отображает содержимое `index.html` файла, который вы изменили на **панели "Источники".**</span><span class="sxs-lookup"><span data-stu-id="f5607-202">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="f5607-203">Вкладка **"Быстрый** источник" позволяет редактировать редактор на панели **"Источники",** чтобы можно было редактировать файлы, открыв другие панели.</span><span class="sxs-lookup"><span data-stu-id="f5607-203">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Открытие вкладки "Экспресс-источник" с помощью меню команд" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="f5607-205">Открытие **вкладки "Экспресс-источник"** с **помощью меню команд**</span><span class="sxs-lookup"><span data-stu-id="f5607-205">Open the **Quick Source** tab using **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f5607-206">Нажмите `Control` + `P` кнопку \(Windows\) `Command` + `P` или \(macOS\), чтобы открыть **диалоговое окно "Открыть** файл".</span><span class="sxs-lookup"><span data-stu-id="f5607-206">Select `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="f5607-207">См. на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="f5607-207">See the following figure.</span></span>  
1.  <span data-ttu-id="f5607-208">Введите `script` и выберите \*\*приложение/script.js. \*\*</span><span class="sxs-lookup"><span data-stu-id="f5607-208">Type `script`, then select **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Открытие script.js с помощью диалогового окна "Открытие файла"" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="f5607-210">`script.js`Открытие файла с **помощью диалогового окна "Открытие** файла"</span><span class="sxs-lookup"><span data-stu-id="f5607-210">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f5607-211">Ссылка `Save Changes To Disk With Workspaces` в демонстрации регулярно применяется к ссылке.</span><span class="sxs-lookup"><span data-stu-id="f5607-211">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="f5607-212">Добавьте следующий код внизу на **вкладкеscript.js"Быстрый** **источник".**</span><span class="sxs-lookup"><span data-stu-id="f5607-212">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="f5607-213">Выберите `Control` + `S` \(Windows\) `Command` + `S` или \(macOS\), чтобы сохранить изменение.</span><span class="sxs-lookup"><span data-stu-id="f5607-213">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="f5607-214">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="f5607-214">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f5607-215">Ссылка на странице теперь выделена курсивом.</span><span class="sxs-lookup"><span data-stu-id="f5607-215">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Ссылка на странице теперь выделена курсивом" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="f5607-217">Ссылка на странице теперь выделена курсивом</span><span class="sxs-lookup"><span data-stu-id="f5607-217">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f5607-218">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f5607-218">Next steps</span></span>  

<span data-ttu-id="f5607-219">Используйте то, что вы узнали в этом учебнике, чтобы настроить рабочие области в своем проекте.</span><span class="sxs-lookup"><span data-stu-id="f5607-219">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
    -->  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS | Документы Майкрософт"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Демонстрация файлов рабочих областей | Глитский"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Содержимое CSS: касание таблиц стилей | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Начало работы с Веб-браузером | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Работа с простой локальным HTTP-сервером | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM — веб-API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Общие сведения об исходных картах | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Порт \(компьютеры\) - Википедия"  

> [!NOTE]
> <span data-ttu-id="f5607-228">Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]</span><span class="sxs-lookup"><span data-stu-id="f5607-228">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f5607-229">Исходная страница [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="f5607-229">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f5607-231">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f5607-231">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

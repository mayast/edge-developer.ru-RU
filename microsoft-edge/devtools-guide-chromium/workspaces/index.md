---
title: Редактирование файлов с помощью рабочих областей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601854"
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







# <span data-ttu-id="d33af-103">Редактирование файлов с помощью рабочих областей</span><span class="sxs-lookup"><span data-stu-id="d33af-103">Edit Files With Workspaces</span></span>   



> [!NOTE]
> <span data-ttu-id="d33af-104">Цель этого учебника — предоставить практические рекомендации по настройке и использованию рабочих областей, чтобы можно было использовать рабочие области в своих проектах.</span><span class="sxs-lookup"><span data-stu-id="d33af-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="d33af-105">Вы можете сохранить изменения в исходном коде на локальном компьютере, который вы сделали в DevTools после включения рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="d33af-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!CAUTION]
> <span data-ttu-id="d33af-106">**Предварительные условия**: перед началом работы с этим учебником следует знать, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="d33af-106">**Prerequisites**: Before beginning this tutorial, you should know how to:</span></span>  
> *   [<span data-ttu-id="d33af-107">Создание веб-страниц с помощью HTML, CSS и JavaScript</span><span class="sxs-lookup"><span data-stu-id="d33af-107">Use HTML, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="d33af-108">Использование DevTools для внесения основных изменений в CSS</span><span class="sxs-lookup"><span data-stu-id="d33af-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="d33af-109">Запуск локального веб-сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="d33af-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="d33af-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="d33af-110">Overview</span></span>   

<span data-ttu-id="d33af-111">Рабочие области позволяют сохранить изменения, внесенные в Devtools, в локальную копию того же файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d33af-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="d33af-112">Например, предположим, что:</span><span class="sxs-lookup"><span data-stu-id="d33af-112">For example, suppose:</span></span>  

*   <span data-ttu-id="d33af-113">У вас есть исходный код для вашего сайта на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="d33af-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="d33af-114">Вы запускаете локальный веб-сервер из каталога исходного кода, чтобы сайт был доступен по адресу `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="d33af-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="d33af-115">Вы открыли `localhost:8080` приложение Microsoft EDGE и используете DevTools для изменения CSS-сайта.</span><span class="sxs-lookup"><span data-stu-id="d33af-115">You opened `localhost:8080`  in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="d33af-116">После включения рабочих областей изменения в CSS, внесенные в DevTools, сохраняются в исходном коде на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="d33af-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="d33af-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="d33af-117">Limitations</span></span>   

<span data-ttu-id="d33af-118">При использовании современной платформы, скорее всего, она преобразует исходный код из формата, который легко поддерживать в формате, который оптимизирован для выполнения как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="d33af-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  
<span data-ttu-id="d33af-119">В рабочих областях обычно можно сопоставить оптимизированный код с первоначальным исходным кодом с помощью [карт исходного][TreehouseBlogSourceMaps]кода.</span><span class="sxs-lookup"><span data-stu-id="d33af-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="d33af-120">Однако между платформами есть множество вариантов использования карт исходного кода.</span><span class="sxs-lookup"><span data-stu-id="d33af-120">But there is a lot of variation between frameworks over how they use source maps.</span></span>  <span data-ttu-id="d33af-121">Devtools просто поддерживает все варианты.</span><span class="sxs-lookup"><span data-stu-id="d33af-121">Devtools simply does support all the variations.</span></span>  

<span data-ttu-id="d33af-122">Рабочие области не работают с этими платформами:</span><span class="sxs-lookup"><span data-stu-id="d33af-122">Workspaces is known to not work with these frameworks:</span></span>  

*   <span data-ttu-id="d33af-123">Приложение "Создание реагируй"</span><span class="sxs-lookup"><span data-stu-id="d33af-123">Create React App</span></span>  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## <span data-ttu-id="d33af-124">Связанная функция: локальные переопределения</span><span class="sxs-lookup"><span data-stu-id="d33af-124">Related feature: Local Overrides</span></span>   

<span data-ttu-id="d33af-125">**Локальные переопределения** — это еще одна функция DevTools, похожая на рабочие области.</span><span class="sxs-lookup"><span data-stu-id="d33af-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="d33af-126">Используйте локальные переопределения, если вы хотите поэкспериментировать с изменениями на странице, и вам нужно увидеть эти изменения при загрузке страницы, но вы не хотите сопоставлять изменения в исходном коде страницы.</span><span class="sxs-lookup"><span data-stu-id="d33af-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see those changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="d33af-127">Действие 1: Настройка</span><span class="sxs-lookup"><span data-stu-id="d33af-127">Step 1: Setup</span></span>   

<span data-ttu-id="d33af-128">Следуйте этим учебником, чтобы получить практические навыки работы с рабочими областями.</span><span class="sxs-lookup"><span data-stu-id="d33af-128">Complete this tutorial to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="d33af-129">Настройка ролика</span><span class="sxs-lookup"><span data-stu-id="d33af-129">Set up the demo</span></span>   

1.  <span data-ttu-id="d33af-130">[Откройте демонстрацию][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="d33af-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### <span data-ttu-id="d33af-131">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="d33af-131">Figure 1</span></span>  
    > <span data-ttu-id="d33af-132">Проект с сбоев ![][ImageGlitchProject]</span><span class="sxs-lookup"><span data-stu-id="d33af-132">A Glitch project ![A Glitch project][ImageGlitchProject]</span></span>  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="d33af-133">Создайте `app` каталог на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="d33af-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="d33af-134">Сохраняйте копии файлов в `workspaces-demo` каталоге.</span><span class="sxs-lookup"><span data-stu-id="d33af-134">Save copies of the files in the `workspaces-demo` directory.</span></span>  <span data-ttu-id="d33af-135">В оставшейся части этого учебника этот каталог называется `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="d33af-135">For the rest of this tutorial this directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="d33af-136">Запустите локальный веб-сервер в `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="d33af-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="d33af-137">Ниже приведен пример кода для запуска `SimpleHTTPServer` , но вы можете использовать любой предпочитаемый сервер.</span><span class="sxs-lookup"><span data-stu-id="d33af-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  <span data-ttu-id="d33af-138">Откройте вкладку в Microsoft EDGE и перейдите на веб-сайт с локально размещенной версией.</span><span class="sxs-lookup"><span data-stu-id="d33af-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="d33af-139">Доступ к ней можно получить с помощью URL-адреса, например `localhost:8080` или `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="d33af-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="d33af-140">Точный [номер порта][WikiPortURLs] может отличаться от остальных.</span><span class="sxs-lookup"><span data-stu-id="d33af-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    > ##### <span data-ttu-id="d33af-141">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="d33af-141">Figure 2</span></span>  
    > <span data-ttu-id="d33af-142">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="d33af-142">The demo</span></span>  
    > <span data-ttu-id="d33af-143">! [Демонстрация] [ImageDemo]</span><span class="sxs-lookup"><span data-stu-id="d33af-143">![The demo][ImageDemo]</span></span>  

### <span data-ttu-id="d33af-144">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="d33af-144">Set up DevTools</span></span>   

1.  <span data-ttu-id="d33af-145">Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \), чтобы открыть панель **консоли** DevTools.</span><span class="sxs-lookup"><span data-stu-id="d33af-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="d33af-146">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="d33af-146">Figure 3</span></span>  
    > <span data-ttu-id="d33af-147">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="d33af-147">The **Console** panel</span></span>  
    > <span data-ttu-id="d33af-148">! [Панель консоли] [ImageConsolePanel]</span><span class="sxs-lookup"><span data-stu-id="d33af-148">![The Console panel][ImageConsolePanel]</span></span>  

1.  <span data-ttu-id="d33af-149">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="d33af-149">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="d33af-150">Откройте вкладку **FileSystem (файловая система** ).</span><span class="sxs-lookup"><span data-stu-id="d33af-150">Click the **Filesystem** tab.</span></span>  
    
    > ##### <span data-ttu-id="d33af-151">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="d33af-151">Figure 4</span></span>  
    > <span data-ttu-id="d33af-152">Вкладка " **Файловая система** "</span><span class="sxs-lookup"><span data-stu-id="d33af-152">The **Filesystem** tab</span></span>  
    > <span data-ttu-id="d33af-153">! [Вкладка FileSystem] [ImageFilesystem]</span><span class="sxs-lookup"><span data-stu-id="d33af-153">![The Filesystem tab][ImageFilesystem]</span></span>  

1.  <span data-ttu-id="d33af-154">Нажмите кнопку **Добавить папку в рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="d33af-154">Click **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="d33af-155">Выберите `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="d33af-155">Select `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="d33af-156">Нажмите кнопку **Разрешить** , чтобы предоставить DevTools разрешение на чтение и запись в каталог.</span><span class="sxs-lookup"><span data-stu-id="d33af-156">Click **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="d33af-157">На вкладке **FileSystem** теперь есть зеленая точка рядом с `index.html` , `script.js` и `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="d33af-157">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="d33af-158">Эти зеленые точки означают, что в DevTools установлено соответствие между сетевыми ресурсами страницы и файлами в `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="d33af-158">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    > ##### <span data-ttu-id="d33af-159">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="d33af-159">Figure 5</span></span>  
    > <span data-ttu-id="d33af-160">На вкладке **FileSystem** теперь показано соответствие между локальными и сетевыми файлами.</span><span class="sxs-lookup"><span data-stu-id="d33af-160">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    > <span data-ttu-id="d33af-161">! [На вкладке FileSystem теперь отображается соответствие между локальными файлами и сетью] [ImageMapping]</span><span class="sxs-lookup"><span data-stu-id="d33af-161">![The Filesystem tab now shows a mapping between the local files and the network ones][ImageMapping]</span></span>  

## <span data-ttu-id="d33af-162">Шаг 2: сохранение изменений CSS на диске</span><span class="sxs-lookup"><span data-stu-id="d33af-162">Step 2: Save a CSS change to disk</span></span>   

1.  <span data-ttu-id="d33af-163">Open (открыть) `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="d33af-163">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="d33af-164">`color` `h1` Для свойства элементы задано значение `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="d33af-164">The `color` property of `h1` elements is set to `fuchsia`.</span></span>
    
    > ##### <span data-ttu-id="d33af-165">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="d33af-165">Figure 6</span></span>  
    > <span data-ttu-id="d33af-166">Просмотр `styles.css` в текстовом редакторе</span><span class="sxs-lookup"><span data-stu-id="d33af-166">Viewing `styles.css` in a text editor</span></span>  
    > <span data-ttu-id="d33af-167">! [Просмотр стилей. CSS в текстовом редакторе] [ImageStylesFuchsia]</span><span class="sxs-lookup"><span data-stu-id="d33af-167">![Viewing styles.css in a text editor][ImageStylesFuchsia]</span></span>  


1.  <span data-ttu-id="d33af-168">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="d33af-168">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="d33af-169">Измените значение `color` свойства `<h1>` элемента на предпочтительный цвет.</span><span class="sxs-lookup"><span data-stu-id="d33af-169">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="d33af-170">Помните о том, что для `<h1>` просмотра примененных к нему правил CSS в области **стили** необходимо щелкнуть элемент в **дереве DOM** .</span><span class="sxs-lookup"><span data-stu-id="d33af-170">Remember that you need to click the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="d33af-171">Зеленая точка рядом с `styles.css:1` ней означает, что все изменения, внесенные вами, сопоставлены `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="d33af-171">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    > ##### <span data-ttu-id="d33af-172">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="d33af-172">Figure 7</span></span>  
    > <span data-ttu-id="d33af-173">Зеленый индикатор, связанный с файлом</span><span class="sxs-lookup"><span data-stu-id="d33af-173">The green indicator that the file is linked</span></span>  
    > <span data-ttu-id="d33af-174">! [Зеленый индикатор, связанный с файлом] [ImageStylesGreen]</span><span class="sxs-lookup"><span data-stu-id="d33af-174">![The green indicator that the file is linked][ImageStylesGreen]</span></span>  

1.  <span data-ttu-id="d33af-175">`styles.css`Снова откройте текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="d33af-175">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="d33af-176">`color`Свойству будет присвоена предпочтительный цвет.</span><span class="sxs-lookup"><span data-stu-id="d33af-176">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="d33af-177">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="d33af-177">Reload the page.</span></span>  <span data-ttu-id="d33af-178">Цвет `<h1>` элемента по-прежнему установлен на предпочтительный цвет.</span><span class="sxs-lookup"><span data-stu-id="d33af-178">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="d33af-179">Это происходит потому, что после внесения изменений DevTools сохраняет изменения на диск.</span><span class="sxs-lookup"><span data-stu-id="d33af-179">This works because when you made the change, DevTools saved the change to disk.</span></span>  <span data-ttu-id="d33af-180">А затем, когда вы перезагрузите страницу, локальный сервер сослужил измененную копию файла с диска.</span><span class="sxs-lookup"><span data-stu-id="d33af-180">And then, when you reloaded the page, your local server served the modified copy of the file from disk.</span></span>  

## <span data-ttu-id="d33af-181">Шаг 3: сохранение изменений HTML на диске</span><span class="sxs-lookup"><span data-stu-id="d33af-181">Step 3: Save an HTML change to disk</span></span>   

### <span data-ttu-id="d33af-182">Изменение HTML на панели "элементы"</span><span class="sxs-lookup"><span data-stu-id="d33af-182">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="d33af-183">Вы можете внести изменения в HTML-код с панели элементов, но ваши изменения в дереве DOM не сохраняются на диск и влияют только на текущий сеанс браузера.</span><span class="sxs-lookup"><span data-stu-id="d33af-183">You may make changes to the HTML from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  
<span data-ttu-id="d33af-184">Дерево DOM не является HTML-кодом.</span><span class="sxs-lookup"><span data-stu-id="d33af-184">The DOM tree is not HTML.</span></span>  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### <span data-ttu-id="d33af-185">Изменение HTML на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="d33af-185">Change HTML from the Sources panel</span></span>   

<span data-ttu-id="d33af-186">Если вы хотите сохранить изменения в HTML-коде страницы, сделайте это с помощью панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="d33af-186">If you want to save a change to the HTML of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="d33af-187">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="d33af-187">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="d33af-188">Откройте вкладку **страница** .</span><span class="sxs-lookup"><span data-stu-id="d33af-188">Click the **Page** tab.</span></span>  
1.  <span data-ttu-id="d33af-189">Нажмите кнопку **(указатель)**.</span><span class="sxs-lookup"><span data-stu-id="d33af-189">Click **(index)**.</span></span>  <span data-ttu-id="d33af-190">Откроется HTML-код для страницы.</span><span class="sxs-lookup"><span data-stu-id="d33af-190">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="d33af-191">Заменить `<h1>Workspaces Demo</h1>` на `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="d33af-191">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="d33af-192">Смотрите [Рисунок 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="d33af-192">See [Figure 8](#figure-8).</span></span>  
1.  <span data-ttu-id="d33af-193">`Control` + `S` Чтобы сохранить изменения, нажмите клавиши \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d33af-193">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="d33af-194">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="d33af-194">Reload the page.</span></span>  <span data-ttu-id="d33af-195">`<h1>`Элемент по-прежнему отображается в новом тексте.</span><span class="sxs-lookup"><span data-stu-id="d33af-195">The `<h1>` element is still displaying the new text.</span></span>  
    
    > ##### <span data-ttu-id="d33af-196">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="d33af-196">Figure 8</span></span>  
    > <span data-ttu-id="d33af-197">Для строки 12 установлено значение</span><span class="sxs-lookup"><span data-stu-id="d33af-197">Line 12 has been set to</span></span> `I ❤️  Cake`  
    > <span data-ttu-id="d33af-198">! [Изменение HTML-кода на панели «источники»] [ImageSourcesCakeHTML]</span><span class="sxs-lookup"><span data-stu-id="d33af-198">![Changing HTML from the Sources panel][ImageSourcesCakeHTML]</span></span>  

1.  <span data-ttu-id="d33af-199">Open (открыть) `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="d33af-199">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="d33af-200">`<h1>`Элемент включает новый текст.</span><span class="sxs-lookup"><span data-stu-id="d33af-200">The `<h1>` element contains the new text.</span></span>  

## <span data-ttu-id="d33af-201">Шаг 4: сохранение изменений JavaScript на диске</span><span class="sxs-lookup"><span data-stu-id="d33af-201">Step 4: Save a JavaScript change to disk</span></span>   

<span data-ttu-id="d33af-202">Панель « **источники** » — это также место, где можно вносить изменения в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d33af-202">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="d33af-203">Но иногда вам нужно получить доступ к другим панелям, таким как панель **элементов** или панель **консоли** , при внесении изменений на сайт.</span><span class="sxs-lookup"><span data-stu-id="d33af-203">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="d33af-204">На панели « **источники** » есть способ открытия рядом с другими панелями.</span><span class="sxs-lookup"><span data-stu-id="d33af-204">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="d33af-205">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="d33af-205">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="d33af-206">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d33af-206">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="d33af-207">Откроется **меню команд** .</span><span class="sxs-lookup"><span data-stu-id="d33af-207">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="d33af-208">Введите текст `QS` и выберите параметр **Показать быстрый источник**.</span><span class="sxs-lookup"><span data-stu-id="d33af-208">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="d33af-209">В нижней части окна DevTools теперь есть вкладка **быстрый источник** .  На вкладке отображается содержимое `index.html` , которое является последним файлом, измененным на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="d33af-209">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="d33af-210">На вкладке **быстрый источник** вы можете открыть редактор из панели **источники** , чтобы можно было редактировать файлы, не открывая другие панели.</span><span class="sxs-lookup"><span data-stu-id="d33af-210">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    > ##### <span data-ttu-id="d33af-211">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="d33af-211">Figure 9</span></span>  
    > <span data-ttu-id="d33af-212">Открытие вкладки " **быстрый источник** " с помощью **меню команд**</span><span class="sxs-lookup"><span data-stu-id="d33af-212">Opening the **Quick Source** tab using the **Command Menu**</span></span>  
    > <span data-ttu-id="d33af-213">! [Открытие вкладки "быстрый источник" с помощью меню "команды"] [ImageCommandMenuQuickSource]</span><span class="sxs-lookup"><span data-stu-id="d33af-213">![Opening the Quick Source tab using Command Menu][ImageCommandMenuQuickSource]</span></span>  

1.  <span data-ttu-id="d33af-214">`Control` + `P` `Command` + `P` Чтобы открыть диалоговое окно " **Открытие файла** ", нажмите клавиши \ (Windows \) или \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d33af-214">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="d33af-215">Смотрите [Рисунок 10](#figure-10).</span><span class="sxs-lookup"><span data-stu-id="d33af-215">See [Figure 10](#figure-10).</span></span>  
1.  <span data-ttu-id="d33af-216">Введите `script` команду **app/script. js**.</span><span class="sxs-lookup"><span data-stu-id="d33af-216">Type `script`, then select **app/script.js**.</span></span>  
    
    > ##### <span data-ttu-id="d33af-217">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="d33af-217">Figure 10</span></span>  
    > <span data-ttu-id="d33af-218">Открытие `script.js` с помощью диалогового окна " **Открыть файл** "</span><span class="sxs-lookup"><span data-stu-id="d33af-218">Opening `script.js` using the **Open File** dialog</span></span>  
    > <span data-ttu-id="d33af-219">! [Открытие сценария. js с помощью диалогового окна "Открытие файла"] [ImageOpenFileDialog]</span><span class="sxs-lookup"><span data-stu-id="d33af-219">![Opening script.js using the Open File dialog][ImageOpenFileDialog]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d33af-220">`Save Changes To Disk With Workspaces`Ссылка в демонстрационной видеоролика будет регулярно применена.</span><span class="sxs-lookup"><span data-stu-id="d33af-220">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="d33af-221">Добавьте следующий код в нижнюю часть **сценария. js** с помощью вкладки " **быстрый источник** ".</span><span class="sxs-lookup"><span data-stu-id="d33af-221">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="d33af-222">`Control` + `S` Чтобы сохранить изменения, нажмите клавиши \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d33af-222">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="d33af-223">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="d33af-223">Reload the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d33af-224">Ссылка на странице теперь будет курсивной.</span><span class="sxs-lookup"><span data-stu-id="d33af-224">The link on the page is now italic.</span></span>
    
    > ##### <span data-ttu-id="d33af-225">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="d33af-225">Figure 11</span></span>  
    > <span data-ttu-id="d33af-226">Ссылка на странице теперь курсивом</span><span class="sxs-lookup"><span data-stu-id="d33af-226">The link on the page is now italic</span></span>  
    > <span data-ttu-id="d33af-227">! [Ссылка на странице теперь курсивом] [ImageScriptItalic]</span><span class="sxs-lookup"><span data-stu-id="d33af-227">![The link on the page is now italic][ImageScriptItalic]</span></span>  

## <span data-ttu-id="d33af-228">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="d33af-228">Next steps</span></span>   

<span data-ttu-id="d33af-229">С помощью этого учебника вы можете настроить рабочие области в проекте.</span><span class="sxs-lookup"><span data-stu-id="d33af-229">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Рисунок 1: неработающий проект с именем, созданным случайным образом"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo.MSFT.png "Рисунок 2: демонстрационный ролик"  
[ImageConsolePanel]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Console.MSFT.png "Рисунок 3: панель консоли"  
[ImageFilesystem]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-FileSystem.MSFT.png "Рисунок 4: вкладка" FileSystem ""  
[ImageMapping]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-FileSystem-Folder.MSFT.png "Рисунок 5: теперь на вкладке FileSystem показано соответствие между локальными и сетевыми файлами.  
[ImageStylesFuchsia]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-FileSystem-CSS.MSFT.png "Рисунок 6: Просмотр стилей. CSS в текстовом редакторе"  
[ImageStylesGreen]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Elements-Styles-CSS.MSFT.png "Рисунок 7: зеленый индикатор, связанный с файлом"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-Page-H1.MSFT.png "Рисунок 8: изменение HTML на панели" источники "  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Search-Show-Quick-Source.MSFT.png "Рисунок 9: Открытие вкладки" быстрый источник "с помощью командного меню  
[ImageOpenFileDialog]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Search-script.MSFT.png "Рисунок 10: открытие сценария. js с помощью диалогового окна" открыть файл "  
[ImageScriptItalic]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Elements-Styles-Quick-Source-script.MSFT.png "Рисунок 11: ссылка на странице теперь курсивом"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Рабочие области — демонстрационные файлы | Цепь"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Content-CSS: Каскадные таблицы стилей | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Начало работы с Интернетом | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Выполнение простого локального HTTP-сервера | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM — веб-API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Общие сведения о картах исходного кода | Блог Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Порт \ (компьютерная сеть \) — Википедии"  

> [!NOTE]
> <span data-ttu-id="d33af-249">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d33af-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d33af-250">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d33af-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d33af-252">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d33af-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

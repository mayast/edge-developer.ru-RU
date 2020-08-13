---
title: Редактирование файлов с помощью рабочих областей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/31/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7cafa2b186d151a478fa532cdac49ae46f2120c3
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926566"
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

# <span data-ttu-id="c9a83-103">Редактирование файлов с помощью рабочих областей</span><span class="sxs-lookup"><span data-stu-id="c9a83-103">Edit Files With Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="c9a83-104">Цель этого учебника — предоставить практические рекомендации по настройке и использованию рабочих областей, чтобы можно было использовать рабочие области в своих проектах.</span><span class="sxs-lookup"><span data-stu-id="c9a83-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="c9a83-105">Вы можете сохранить изменения в исходном коде на локальном компьютере, который вы сделали в DevTools после включения рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="c9a83-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!CAUTION]
> <span data-ttu-id="c9a83-106">**Предварительные условия**: перед началом работы с этим учебником следует знать, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="c9a83-106">**Prerequisites**: Before beginning this tutorial, you should know how to:</span></span>  
> *   [<span data-ttu-id="c9a83-107">Создание веб-страниц с помощью HTML, CSS и JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9a83-107">Use HTML, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="c9a83-108">Использование DevTools для внесения основных изменений в CSS</span><span class="sxs-lookup"><span data-stu-id="c9a83-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="c9a83-109">Запуск локального веб-сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="c9a83-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="c9a83-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="c9a83-110">Overview</span></span>  

<span data-ttu-id="c9a83-111">Рабочие области позволяют сохранить изменения, внесенные в Devtools, в локальную копию того же файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c9a83-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="c9a83-112">Например, предположим, что:</span><span class="sxs-lookup"><span data-stu-id="c9a83-112">For example, suppose:</span></span>  

*   <span data-ttu-id="c9a83-113">У вас есть исходный код для вашего сайта на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="c9a83-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="c9a83-114">Вы запускаете локальный веб-сервер из каталога исходного кода, чтобы сайт был доступен по адресу `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="c9a83-115">Вы открыли `localhost:8080` приложение Microsoft EDGE и используете DevTools для изменения CSS-сайта.</span><span class="sxs-lookup"><span data-stu-id="c9a83-115">You opened `localhost:8080`  in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="c9a83-116">После включения рабочих областей изменения в CSS, внесенные в DevTools, сохраняются в исходном коде на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="c9a83-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="c9a83-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="c9a83-117">Limitations</span></span>  

<span data-ttu-id="c9a83-118">При использовании современной платформы, скорее всего, она преобразует исходный код из формата, который легко поддерживать в формате, который оптимизирован для выполнения как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="c9a83-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  
<span data-ttu-id="c9a83-119">В рабочих областях обычно можно сопоставить оптимизированный код с первоначальным исходным кодом с помощью [карт исходного][TreehouseBlogSourceMaps]кода.</span><span class="sxs-lookup"><span data-stu-id="c9a83-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="c9a83-120">Однако между платформами есть множество вариантов использования карт исходного кода.</span><span class="sxs-lookup"><span data-stu-id="c9a83-120">But there is a lot of variation between frameworks over how they use source maps.</span></span>  <span data-ttu-id="c9a83-121">Devtools просто не поддерживает все варианты.</span><span class="sxs-lookup"><span data-stu-id="c9a83-121">Devtools simply does not support all of the variations.</span></span>  

<span data-ttu-id="c9a83-122">Рабочие области не работают с этими платформами:</span><span class="sxs-lookup"><span data-stu-id="c9a83-122">Workspaces is known to not work with these frameworks:</span></span>  

*   <span data-ttu-id="c9a83-123">Приложение "Создание реагируй"</span><span class="sxs-lookup"><span data-stu-id="c9a83-123">Create React App</span></span>  
    
    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <span data-ttu-id="c9a83-124">Связанная функция: локальные переопределения</span><span class="sxs-lookup"><span data-stu-id="c9a83-124">Related feature: Local Overrides</span></span>  

<span data-ttu-id="c9a83-125">**Локальные переопределения** — это еще одна функция DevTools, похожая на рабочие области.</span><span class="sxs-lookup"><span data-stu-id="c9a83-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="c9a83-126">Используйте локальные переопределения, если вы хотите поэкспериментировать с изменениями на странице, и вам нужно увидеть эти изменения при загрузке страницы, но вы не хотите сопоставлять изменения в исходном коде страницы.</span><span class="sxs-lookup"><span data-stu-id="c9a83-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see those changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="c9a83-127">Шаг 1: Настройка</span><span class="sxs-lookup"><span data-stu-id="c9a83-127">Step 1: Set-up</span></span>  

<span data-ttu-id="c9a83-128">Следуйте этим учебником, чтобы получить практические навыки работы с рабочими областями.</span><span class="sxs-lookup"><span data-stu-id="c9a83-128">Complete this tutorial to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="c9a83-129">Настройка ролика</span><span class="sxs-lookup"><span data-stu-id="c9a83-129">Set up the demo</span></span>  

1.  <span data-ttu-id="c9a83-130">[Откройте демонстрацию][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="c9a83-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Несбойный проект" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="c9a83-132">Несбойный проект</span><span class="sxs-lookup"><span data-stu-id="c9a83-132">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="c9a83-133">Создайте `app` каталог на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="c9a83-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="c9a83-134">Сохраняйте копии файлов в `workspaces-demo` каталоге.</span><span class="sxs-lookup"><span data-stu-id="c9a83-134">Save copies of the files in the `workspaces-demo` directory.</span></span>  <span data-ttu-id="c9a83-135">В оставшейся части этого учебника этот каталог называется `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-135">For the rest of this tutorial this directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="c9a83-136">Запустите локальный веб-сервер в `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="c9a83-137">Ниже приведен пример кода для запуска `SimpleHTTPServer` , но вы можете использовать любой предпочитаемый сервер.</span><span class="sxs-lookup"><span data-stu-id="c9a83-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
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
    
1.  <span data-ttu-id="c9a83-138">Откройте вкладку в Microsoft EDGE и перейдите на веб-сайт с локально размещенной версией.</span><span class="sxs-lookup"><span data-stu-id="c9a83-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="c9a83-139">Доступ к ней можно получить с помощью URL-адреса, например `localhost:8080` или `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="c9a83-140">Точный [номер порта][WikiPortURLs] может отличаться от остальных.</span><span class="sxs-lookup"><span data-stu-id="c9a83-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Демонстрация" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="c9a83-142">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="c9a83-142">The demo</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="c9a83-143">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="c9a83-143">Set up DevTools</span></span>  

1.  <span data-ttu-id="c9a83-144">Выберите `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \), чтобы открыть панель **консоли** DevTools.</span><span class="sxs-lookup"><span data-stu-id="c9a83-144">Select `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Панель консоли" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="c9a83-146">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="c9a83-146">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c9a83-147">Перейдите на вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="c9a83-147">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="c9a83-148">Перейдите на вкладку **FileSystem (файловая система** ).</span><span class="sxs-lookup"><span data-stu-id="c9a83-148">Choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Вкладка "файловая система"" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="c9a83-150">Вкладка " **Файловая система** "</span><span class="sxs-lookup"><span data-stu-id="c9a83-150">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c9a83-151">Выберите команду **Добавить папку в рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="c9a83-151">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="c9a83-152">Ввод `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-152">Enter `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="c9a83-153">Нажмите кнопку **Разрешить** , чтобы предоставить DevTools разрешение на чтение и запись в каталог.</span><span class="sxs-lookup"><span data-stu-id="c9a83-153">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="c9a83-154">На вкладке **FileSystem** теперь есть зеленая точка рядом с `index.html` , `script.js` и `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-154">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="c9a83-155">Эти зеленые точки означают, что в DevTools установлено соответствие между сетевыми ресурсами страницы и файлами в `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-155">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="На вкладке FileSystem теперь показано соответствие между локальными и сетевыми файлами." lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="c9a83-157">На вкладке **FileSystem** теперь показано соответствие между локальными и сетевыми файлами.</span><span class="sxs-lookup"><span data-stu-id="c9a83-157">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c9a83-158">Шаг 2: сохранение изменений CSS на диске</span><span class="sxs-lookup"><span data-stu-id="c9a83-158">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="c9a83-159">Open (открыть) `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-159">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c9a83-160">`color` `h1` Для свойства элементы задано значение `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-160">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Просмотр стилей. CSS в текстовом редакторе" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="c9a83-162">Просмотр `styles.css` в текстовом редакторе</span><span class="sxs-lookup"><span data-stu-id="c9a83-162">Viewing `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c9a83-163">Перейдите на вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="c9a83-163">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="c9a83-164">Измените значение `color` свойства `<h1>` элемента на предпочтительный цвет.</span><span class="sxs-lookup"><span data-stu-id="c9a83-164">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="c9a83-165">Помните о том, что для `<h1>` просмотра примененных к нему правил CSS в области **стили** необходимо выбрать элемент в **дереве DOM** .</span><span class="sxs-lookup"><span data-stu-id="c9a83-165">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="c9a83-166">Зеленая точка рядом с `styles.css:1` ней означает, что все изменения, внесенные вами, сопоставлены `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-166">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Зеленый индикатор, связанный с файлом" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="c9a83-168">Зеленый индикатор, связанный с файлом</span><span class="sxs-lookup"><span data-stu-id="c9a83-168">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c9a83-169">`styles.css`Снова откройте текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="c9a83-169">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="c9a83-170">`color`Свойству будет присвоена предпочтительный цвет.</span><span class="sxs-lookup"><span data-stu-id="c9a83-170">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="c9a83-171">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="c9a83-171">Reload the page.</span></span>  <span data-ttu-id="c9a83-172">Цвет `<h1>` элемента по-прежнему установлен на предпочтительный цвет.</span><span class="sxs-lookup"><span data-stu-id="c9a83-172">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="c9a83-173">Это происходит потому, что после внесения изменений DevTools сохраняет изменения на диск.</span><span class="sxs-lookup"><span data-stu-id="c9a83-173">This works because when you made the change, DevTools saved the change to disk.</span></span>  <span data-ttu-id="c9a83-174">А затем, когда вы перезагрузите страницу, локальный сервер сослужил измененную копию файла с диска.</span><span class="sxs-lookup"><span data-stu-id="c9a83-174">And then, when you reloaded the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <span data-ttu-id="c9a83-175">Шаг 3: сохранение изменений HTML на диске</span><span class="sxs-lookup"><span data-stu-id="c9a83-175">Step 3: Save an HTML change to disk</span></span>  

### <span data-ttu-id="c9a83-176">Изменение HTML на панели "элементы"</span><span class="sxs-lookup"><span data-stu-id="c9a83-176">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="c9a83-177">Вы можете внести изменения в HTML-код с панели элементов, но ваши изменения в дереве DOM не сохраняются на диск и влияют только на текущий сеанс браузера.</span><span class="sxs-lookup"><span data-stu-id="c9a83-177">You may make changes to the HTML from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  
<span data-ttu-id="c9a83-178">Дерево DOM не является HTML-кодом.</span><span class="sxs-lookup"><span data-stu-id="c9a83-178">The DOM tree is not HTML.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Double-click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempting to change HTML from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    :::image-end:::  
    
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

### <span data-ttu-id="c9a83-179">Изменение HTML на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="c9a83-179">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="c9a83-180">Если вы хотите сохранить изменения в HTML-коде страницы, сделайте это с помощью панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="c9a83-180">If you want to save a change to the HTML of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="c9a83-181">Перейдите на вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="c9a83-181">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="c9a83-182">Перейдите на вкладку **страница** .</span><span class="sxs-lookup"><span data-stu-id="c9a83-182">Choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="c9a83-183">Выберите **(предметный указатель)**.</span><span class="sxs-lookup"><span data-stu-id="c9a83-183">Choose **(index)**.</span></span>  <span data-ttu-id="c9a83-184">Откроется HTML-код для страницы.</span><span class="sxs-lookup"><span data-stu-id="c9a83-184">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="c9a83-185">Заменить `<h1>Workspaces Demo</h1>` на `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-185">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="c9a83-186">Смотрите на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c9a83-186">See the following figure.</span></span>  
1.  <span data-ttu-id="c9a83-187">Выберите `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \), чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="c9a83-187">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="c9a83-188">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="c9a83-188">Reload the page.</span></span>  <span data-ttu-id="c9a83-189">`<h1>`Элемент по-прежнему отображается в новом тексте.</span><span class="sxs-lookup"><span data-stu-id="c9a83-189">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Изменение HTML-кода на панели «источники»" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="c9a83-191">Для строки 12 установлено значение</span><span class="sxs-lookup"><span data-stu-id="c9a83-191">Line 12 has been set to</span></span> `I ❤️  Cake`  
    :::image-end:::  
    
1.  <span data-ttu-id="c9a83-192">Open (открыть) `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="c9a83-192">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="c9a83-193">`<h1>`Элемент включает новый текст.</span><span class="sxs-lookup"><span data-stu-id="c9a83-193">The `<h1>` element contains the new text.</span></span>  
    
## <span data-ttu-id="c9a83-194">Шаг 4: сохранение изменений JavaScript на диске</span><span class="sxs-lookup"><span data-stu-id="c9a83-194">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="c9a83-195">Панель « **источники** » — это также место, где можно вносить изменения в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c9a83-195">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="c9a83-196">Но иногда вам нужно получить доступ к другим панелям, таким как панель **элементов** или панель **консоли** , при внесении изменений на сайт.</span><span class="sxs-lookup"><span data-stu-id="c9a83-196">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="c9a83-197">На панели « **источники** » есть способ открытия рядом с другими панелями.</span><span class="sxs-lookup"><span data-stu-id="c9a83-197">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="c9a83-198">Перейдите на вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="c9a83-198">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="c9a83-199">Выберите `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="c9a83-199">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="c9a83-200">Откроется **меню команд** .</span><span class="sxs-lookup"><span data-stu-id="c9a83-200">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="c9a83-201">Введите текст `QS` и выберите параметр **Показать быстрый источник**.</span><span class="sxs-lookup"><span data-stu-id="c9a83-201">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="c9a83-202">В нижней части окна DevTools теперь есть вкладка **быстрый источник** .  На вкладке отображается содержимое `index.html` , которое является последним файлом, измененным на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="c9a83-202">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="c9a83-203">На вкладке **быстрый источник** вы можете открыть редактор из панели **источники** , чтобы можно было редактировать файлы, не открывая другие панели.</span><span class="sxs-lookup"><span data-stu-id="c9a83-203">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Открытие вкладки "быстрый источник" с помощью командного меню" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="c9a83-205">Открытие вкладки " **быстрый источник** " с помощью **меню команд**</span><span class="sxs-lookup"><span data-stu-id="c9a83-205">Opening the **Quick Source** tab using the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c9a83-206">`Control` + `P` `Command` + `P` Чтобы открыть диалоговое окно " **Открытие файла** ", выберите \ (Windows \) или \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="c9a83-206">Select `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="c9a83-207">Смотрите на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c9a83-207">See the following figure.</span></span>  
1.  <span data-ttu-id="c9a83-208">Введите текст и `script` выберите **приложение/script.js**.</span><span class="sxs-lookup"><span data-stu-id="c9a83-208">Type `script`, then select **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Открытие script.js с помощью диалогового окна "Открытие файла"" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="c9a83-210">Открытие `script.js` с помощью диалогового окна " **Открыть файл** "</span><span class="sxs-lookup"><span data-stu-id="c9a83-210">Opening `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c9a83-211">`Save Changes To Disk With Workspaces`Ссылка в демонстрационной видеоролика будет регулярно применена.</span><span class="sxs-lookup"><span data-stu-id="c9a83-211">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="c9a83-212">Добавьте следующий код в нижнюю часть **script.js** с помощью вкладки " **быстрый источник** ".</span><span class="sxs-lookup"><span data-stu-id="c9a83-212">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="c9a83-213">Выберите `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \), чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="c9a83-213">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="c9a83-214">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="c9a83-214">Reload the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c9a83-215">Ссылка на странице теперь будет курсивной.</span><span class="sxs-lookup"><span data-stu-id="c9a83-215">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Ссылка на странице теперь выделена курсивом" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="c9a83-217">Ссылка на странице теперь выделена курсивом</span><span class="sxs-lookup"><span data-stu-id="c9a83-217">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c9a83-218">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c9a83-218">Next steps</span></span>  

<span data-ttu-id="c9a83-219">С помощью этого учебника вы можете настроить рабочие области в проекте.</span><span class="sxs-lookup"><span data-stu-id="c9a83-219">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on these topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md# "Начало просмотра и изменения CSS | Документы Microsoft"  

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
> <span data-ttu-id="c9a83-228">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9a83-228">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c9a83-229">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c9a83-229">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c9a83-231">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9a83-231">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

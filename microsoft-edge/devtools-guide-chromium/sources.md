---
title: Обзор палитры «источники»
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601910"
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
   limitations under the License. -->






# <span data-ttu-id="feae8-103">Обзор палитры «источники»</span><span class="sxs-lookup"><span data-stu-id="feae8-103">Sources Panel Overview</span></span> 



<span data-ttu-id="feae8-104">С помощью панели DevTools **источники** Microsoft EDGE Вы можете:</span><span class="sxs-lookup"><span data-stu-id="feae8-104">Use the Microsoft Edge DevTools **Sources** panel to:</span></span>

*   <span data-ttu-id="feae8-105">[Просмотр файлов](#view-files).</span><span class="sxs-lookup"><span data-stu-id="feae8-105">[View files](#view-files).</span></span>  
*   <span data-ttu-id="feae8-106">[Редактирование CSS и JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="feae8-106">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="feae8-107">[Создавайте и сохраняйте **фрагменты кода** JavaScript](#create-save-and-run-snippets), которые можно запускать на любой странице.</span><span class="sxs-lookup"><span data-stu-id="feae8-107">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="feae8-108">**Фрагменты** аналогичны кнопкам для закладок.</span><span class="sxs-lookup"><span data-stu-id="feae8-108">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="feae8-109">[Отладка JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="feae8-109">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="feae8-110">[Настройте рабочую область](#set-up-a-workspace), чтобы изменения, внесенные в DevTools, сохранялись в коде в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="feae8-110">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  

## <span data-ttu-id="feae8-111">Просмотр файлов</span><span class="sxs-lookup"><span data-stu-id="feae8-111">View files</span></span> 

<span data-ttu-id="feae8-112">Используйте область **страниц** для просмотра всех ресурсов, загруженных страницей.</span><span class="sxs-lookup"><span data-stu-id="feae8-112">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

> ##### <span data-ttu-id="feae8-113">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="feae8-113">Figure 1</span></span>  
> <span data-ttu-id="feae8-114">Область **страницы**</span><span class="sxs-lookup"><span data-stu-id="feae8-114">The **Page** pane</span></span>  
> ![Рисунок 1: область страницы][ImageSourcesPagePane]  

<span data-ttu-id="feae8-116">Упорядочение области **страницы** .</span><span class="sxs-lookup"><span data-stu-id="feae8-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="feae8-117">Верхний уровень, например `top` на [**рис. 1**](#figure-1), представляет [рамку HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="feae8-117">The top-level, such as `top` in [**Figure 1**](#figure-1), represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="feae8-118">Найдите `top` на каждой странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="feae8-118">Find `top` on every page that you visit.</span></span> `top` <span data-ttu-id="feae8-119">представляет рамку основного документа.</span><span class="sxs-lookup"><span data-stu-id="feae8-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="feae8-120">Второй уровень, например `docs.microsoft.com` на [**рисунке 1**](#figure-1), представляет [источник][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="feae8-120">The second-level, such as `docs.microsoft.com` in [**Figure 1**](#figure-1), represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="feae8-121">Третий уровень, четвертый уровень и т. д. — каталоги и ресурсы, загруженные из этого источника.</span><span class="sxs-lookup"><span data-stu-id="feae8-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="feae8-122">Например, на [**рисунке 1**](#figure-1) полный путь `devtools-guide-chromium` к ресурсу</span><span class="sxs-lookup"><span data-stu-id="feae8-122">For example, in [**Figure 1**](#figure-1) the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

<span data-ttu-id="feae8-123">Щелкните файл в области **страницы** , чтобы просмотреть содержимое в области " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="feae8-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="feae8-124">Вы можете просматривать файлы любого типа.</span><span class="sxs-lookup"><span data-stu-id="feae8-124">You may view any type of file.</span></span> <span data-ttu-id="feae8-125">Для изображений вы видите изображение для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="feae8-125">For images, you see a preview of the image.</span></span>  

> ##### <span data-ttu-id="feae8-126">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="feae8-126">Figure 2</span></span>  
> <span data-ttu-id="feae8-127">Просмотр содержимого `a4d10f71.index-docs.js` в области " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="feae8-127">Viewing the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
> ![Рисунок 2.][ImageSourcesEditorPane]  

## <span data-ttu-id="feae8-130">Редактирование CSS и JavaScript</span><span class="sxs-lookup"><span data-stu-id="feae8-130">Edit CSS and JavaScript</span></span> 

<span data-ttu-id="feae8-131">Для изменения CSS и JavaScript используйте область " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="feae8-131">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="feae8-132">DevTools обновляет страницу, чтобы выполнить новый код.</span><span class="sxs-lookup"><span data-stu-id="feae8-132">DevTools updates the page to run your new code.</span></span> <span data-ttu-id="feae8-133">Например, если вы изменяете CSS-файл, добавив правило стиля ниже:</span><span class="sxs-lookup"><span data-stu-id="feae8-133">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="feae8-134">Вы увидите, что изменения вступают в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="feae8-134">You should see that change take effect immediately.</span></span>

> ##### <span data-ttu-id="feae8-135">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="feae8-135">Figure 3</span></span>  
> <span data-ttu-id="feae8-136">Редактирование CSS на панели « **Редактор** » для изменения цвета текста подзаголовка на красный</span><span class="sxs-lookup"><span data-stu-id="feae8-136">Editing CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
> ![Рисунок 3.][ImageEditCSS]  

<span data-ttu-id="feae8-139">Изменения в CSS вступают в силу немедленно, сохранение не требуется.</span><span class="sxs-lookup"><span data-stu-id="feae8-139">CSS changes take effect immediately, no save needed.</span></span> <span data-ttu-id="feae8-140">Чтобы изменения в JavaScript вступили в силу, нажмите клавиши `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="feae8-140">For JavaScript changes to take effect, press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\).</span></span> <span data-ttu-id="feae8-141">DevTools не выполняет повторно сценарий, поэтому изменения, которые вступают в силу, выполняются только в рамках функций.</span><span class="sxs-lookup"><span data-stu-id="feae8-141">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="feae8-142">Например, на [**рисунке 4**](#figure-4) Обратите внимание на `console.log('A')` то, что не выполняется, в то время как оно `console.log('B')` делает.</span><span class="sxs-lookup"><span data-stu-id="feae8-142">For example, in [**Figure 4**](#figure-4) note how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span> <span data-ttu-id="feae8-143">Если после внесения изменений DevTools повторно запустили весь сценарий, он `A` будет записан в журнал на **консоли**.</span><span class="sxs-lookup"><span data-stu-id="feae8-143">If DevTools re-ran the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

> ##### <span data-ttu-id="feae8-144">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="feae8-144">Figure 4</span></span>  
> <span data-ttu-id="feae8-145">Редактирование JavaScript в области " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="feae8-145">Editing JavaScript in the **Editor** pane</span></span>  
> ![Рисунок 4.][ImageEditJS]  

<span data-ttu-id="feae8-148">DevTools удаляет изменения стилей CSS и JavaScript при повторной загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="feae8-148">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span> <span data-ttu-id="feae8-149">Сведения о том, как сохранить изменения в файловой системе, можно найти в разделе [Настройка рабочей области](#set-up-a-workspace) .</span><span class="sxs-lookup"><span data-stu-id="feae8-149">See [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="feae8-150">Создание, сохранение и запуск фрагментов</span><span class="sxs-lookup"><span data-stu-id="feae8-150">Create, save, and run Snippets</span></span> 

<span data-ttu-id="feae8-151">Фрагменты — это сценарии, которые можно запускать на любой странице.</span><span class="sxs-lookup"><span data-stu-id="feae8-151">Snippets are scripts which you may run on any page.</span></span> <span data-ttu-id="feae8-152">Предположим, что вы повторно вводите на **консоли**следующий код, чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли**:</span><span class="sxs-lookup"><span data-stu-id="feae8-152">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="feae8-153">Вместо этого вы можете сохранить этот код во **фрагменте** и выполнить его с помощью нескольких нажатий кнопки, когда вам понадобится.</span><span class="sxs-lookup"><span data-stu-id="feae8-153">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="feae8-154">DevTools сохранит **фрагмент** в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="feae8-154">DevTools saves the **Snippet** to your file system.</span></span>  

> ##### <span data-ttu-id="feae8-155">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="feae8-155">Figure 5</span></span>  
> <span data-ttu-id="feae8-156">**Фрагмент кода** , который вставляет библиотеку jQuery на страницу</span><span class="sxs-lookup"><span data-stu-id="feae8-156">A **Snippet** that inserts the jQuery library into a page</span></span>  
> ![Рисунок 5.][ImageSnippet]  

<span data-ttu-id="feae8-159">Чтобы выполнить **фрагмент кода**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="feae8-159">To run a **Snippet**:</span></span>

*   <span data-ttu-id="feae8-160">Откройте файл с помощью панели **фрагментов** **и нажмите кнопку выполнить** ![ ][ImageRunIcon] .</span><span class="sxs-lookup"><span data-stu-id="feae8-160">Open the file via the **Snippets** pane, and click **Run** ![The Run button][ImageRunIcon].</span></span>  
*   <span data-ttu-id="feae8-161">Откройте **[меню команд][DevtoolsGuideChromiumCommandMenuIndex]**, удалите `>` символ, введите `!` его имя, а затем нажмите клавишу **Snippet** `Enter` .</span><span class="sxs-lookup"><span data-stu-id="feae8-161">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then press `Enter`.</span></span>  

<span data-ttu-id="feae8-162">Дополнительные сведения можно найти в разделе [выполнение фрагментов кода на любой странице][DevtoolsGuideChromiumJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="feae8-162">See [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>


## <span data-ttu-id="feae8-163">Отладка JavaScript</span><span class="sxs-lookup"><span data-stu-id="feae8-163">Debug JavaScript</span></span> 

<span data-ttu-id="feae8-164">Вместо того `console.log()` , чтобы использовать для определения того, где произошел сбой JavaScript, рекомендуется использовать инструменты отладки Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="feae8-164">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span> <span data-ttu-id="feae8-165">Общая идея состоит в том, чтобы установить точку останова, которая является умышленно остановленным местом в вашем коде, и пошаговое руководство по коду — по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="feae8-165">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span> <span data-ttu-id="feae8-166">По мере выполнения кода вы можете просматривать и изменять значения всех текущих заданных свойств и переменных, запускать JavaScript на **консоли**и т. д.</span><span class="sxs-lookup"><span data-stu-id="feae8-166">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="feae8-167">Сведения об отладке в DevTools можно найти в статье Начало [работы с отладкой JavaScript][DevtoolsGuideChromiumJavascriptIndex] .</span><span class="sxs-lookup"><span data-stu-id="feae8-167">See [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

> ##### <span data-ttu-id="feae8-168">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="feae8-168">Figure 6</span></span>  
> <span data-ttu-id="feae8-169">Отладка JavaScript</span><span class="sxs-lookup"><span data-stu-id="feae8-169">Debugging JavaScript</span></span>  
> ![Рисунок 6.][ImageDebugging]  

## <span data-ttu-id="feae8-172">Настройка рабочей области</span><span class="sxs-lookup"><span data-stu-id="feae8-172">Set up a Workspace</span></span> 

<span data-ttu-id="feae8-173">По умолчанию при редактировании файла на панели « **источники** » эти изменения теряются при повторной загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="feae8-173">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="feae8-174">**Рабочие области** позволяют сохранить изменения, внесенные в DevTools, в файловую систему.</span><span class="sxs-lookup"><span data-stu-id="feae8-174">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="feae8-175">По сути, это позволяет использовать DevTools в качестве редактора кода.</span><span class="sxs-lookup"><span data-stu-id="feae8-175">Essentially, this lets you use DevTools as your code editor.</span></span>

<span data-ttu-id="feae8-176">Чтобы приступить к работе, ознакомьтесь со статьей [изменение файлов с помощью рабочих областей][DevtoolsGuideChromiumWorkspacesIndex] .</span><span class="sxs-lookup"><span data-stu-id="feae8-176">See [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Рисунок 1: область страницы"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Рисунок 2: Просмотр содержимого файла a4d10f71. index-docs. js в области "редактор""  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Рисунок 3: Редактирование CSS на панели "редактор" для изменения цвета текста подзаголовка на красный"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Рисунок 4: Редактирование JavaScript в области "редактор""  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Рисунок 5: фрагмент, который вставляет библиотеку jQuery на страницу"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Рисунок 6: Отладка JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Редактирование файлов с помощью рабочих областей"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Современный: HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Кадры | PNG"  

> [!NOTE]
> <span data-ttu-id="feae8-189">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="feae8-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="feae8-190">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/sources) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="feae8-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="feae8-192">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="feae8-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

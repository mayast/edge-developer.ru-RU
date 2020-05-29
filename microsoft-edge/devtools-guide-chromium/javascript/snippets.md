---
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581819"
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





# <span data-ttu-id="3648f-103">Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3648f-103">Run Snippets Of JavaScript On Any Page With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="3648f-104">Если вы обнаружите, что один и тот же код запускается повторно на [консоли][DevtoolsConsoleIndex] , попробуйте сохранить его как фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="3648f-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="3648f-105">Фрагменты — это сценарии, созданные вами на [панели « **источники** »][DevToolsSourcesPanel].</span><span class="sxs-lookup"><span data-stu-id="3648f-105">Snippets are scripts that you author in the [**Sources** panel][DevToolsSourcesPanel].</span></span>  <span data-ttu-id="3648f-106">У них есть доступ к контексту JavaScript на странице, и вы можете запускать их на любой странице.</span><span class="sxs-lookup"><span data-stu-id="3648f-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="3648f-107">Фрагменты — это альтернатива для [Закладка][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="3648f-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="3648f-108">В Firefox DevTools есть функция, похожая на фрагменты, которые называются [блокнотом][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="3648f-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="3648f-109">Например, на [**рисунке 1**](#figure-1) показана домашняя страница DevTools слева и фрагмент исходного кода справа.</span><span class="sxs-lookup"><span data-stu-id="3648f-109">For example, [**Figure 1**](#figure-1) shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

> ##### <span data-ttu-id="3648f-110">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="3648f-110">Figure 1</span></span>  
> <span data-ttu-id="3648f-111">Вид страницы перед выполнением фрагмента</span><span class="sxs-lookup"><span data-stu-id="3648f-111">How the page looks before running the Snippet</span></span>  
> ![Вид страницы перед выполнением фрагмента][ImageSnippetSplitScreen]  

<span data-ttu-id="3648f-113">Исходный код фрагмента на [**рисунке 1**](#figure-1):</span><span class="sxs-lookup"><span data-stu-id="3648f-113">The Snippet source code from [**Figure 1**](#figure-1):</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="3648f-114">[**На рисунке 2**](#figure-2) показано, как выглядит страница после выполнения фрагмента.</span><span class="sxs-lookup"><span data-stu-id="3648f-114">[**Figure 2**](#figure-2) shows how the page looks after running the Snippet.</span></span>  <span data-ttu-id="3648f-115">Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое страницы полностью меняются.</span><span class="sxs-lookup"><span data-stu-id="3648f-115">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

> ##### <span data-ttu-id="3648f-116">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="3648f-116">Figure 2</span></span>  
> <span data-ttu-id="3648f-117">Вид страницы после выполнения фрагмента</span><span class="sxs-lookup"><span data-stu-id="3648f-117">How the page looks after running the Snippet</span></span>  
> ![Вид страницы после выполнения фрагмента][ImageSnippetSplitScreenAfter]  

## <span data-ttu-id="3648f-119">Открытие области "фрагменты кода"</span><span class="sxs-lookup"><span data-stu-id="3648f-119">Open the Snippets pane</span></span>   

<span data-ttu-id="3648f-120">На панели **фрагментов** перечислены ваши фрагменты.</span><span class="sxs-lookup"><span data-stu-id="3648f-120">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="3648f-121">Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .</span><span class="sxs-lookup"><span data-stu-id="3648f-121">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

> ##### <span data-ttu-id="3648f-122">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="3648f-122">Figure 3</span></span>  
> <span data-ttu-id="3648f-123">Область **фрагментов**</span><span class="sxs-lookup"><span data-stu-id="3648f-123">The **Snippets** pane</span></span>  
> ![Область фрагментов][ImageSnippetsPane]  

### <span data-ttu-id="3648f-125">Открытие области фрагментов с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="3648f-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="3648f-126">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="3648f-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="3648f-127">Обычно область **страницы** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3648f-127">The **Page** pane usually opens by default.</span></span>  

    > ##### <span data-ttu-id="3648f-128">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="3648f-128">Figure 4</span></span>  
    > <span data-ttu-id="3648f-129">Панель « **источники** » с открытой областью **страницы** в левой части экрана</span><span class="sxs-lookup"><span data-stu-id="3648f-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    > ![Панель «источники» с открытой областью страницы в левой части экрана][ImageSourcesPageEmpty]  

1.  <span data-ttu-id="3648f-131">Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .</span><span class="sxs-lookup"><span data-stu-id="3648f-131">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="3648f-132">**More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться нажать кнопку Другие вкладки.</span><span class="sxs-lookup"><span data-stu-id="3648f-132">You might need to click **More Tabs** ![More Tabs][ImageMoreTabsIcon] in order to access the **Snippets** option.</span></span>  

### <span data-ttu-id="3648f-133">Открытие области фрагментов с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="3648f-133">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="3648f-134">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3648f-134">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="3648f-135">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3648f-135">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="3648f-136">Начните вводить текст `Snippets` , нажмите кнопку **Показать фрагменты**и нажмите клавишу `Enter` для запуска команды.</span><span class="sxs-lookup"><span data-stu-id="3648f-136">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="3648f-137">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="3648f-137">Figure 5</span></span>  
    > <span data-ttu-id="3648f-138">Команда « **Показать фрагменты** »</span><span class="sxs-lookup"><span data-stu-id="3648f-138">The **Show Snippets** command</span></span>  
    > ![Команда «Показать фрагменты»][ImageShowSnippetsSearch]  

## <span data-ttu-id="3648f-140">Создание фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="3648f-140">Create Snippets</span></span>   

### <span data-ttu-id="3648f-141">Создание фрагмента с помощью панели «источники»</span><span class="sxs-lookup"><span data-stu-id="3648f-141">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="3648f-142">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="3648f-142">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="3648f-143">Нажмите кнопку **создать фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="3648f-143">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="3648f-144">Введите имя для фрагмента, а затем нажмите `Enter` для сохранения.</span><span class="sxs-lookup"><span data-stu-id="3648f-144">Enter a name for your Snippet then press `Enter` to save.</span></span>  

    > ##### <span data-ttu-id="3648f-145">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="3648f-145">Figure 6</span></span>  
    > <span data-ttu-id="3648f-146">Присвоение имени фрагменту</span><span class="sxs-lookup"><span data-stu-id="3648f-146">Naming a Snippet</span></span>  
    > ![Присвоение имени фрагменту][ImageSnippetName]  

### <span data-ttu-id="3648f-148">Создание фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="3648f-148">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="3648f-149">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3648f-149">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="3648f-150">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3648f-150">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="3648f-151">Начните вводить текст `Snippet` , выберите **создать новый фрагмент**, а затем нажмите, `Enter` чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="3648f-151">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="3648f-152">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="3648f-152">Figure 7</span></span>  
    > <span data-ttu-id="3648f-153">Команда для создания нового фрагмента.</span><span class="sxs-lookup"><span data-stu-id="3648f-153">The command for creating a new Snippet</span></span>  
    > ![Команда для создания нового фрагмента.][ImageCreateSnippetSearch]  

<span data-ttu-id="3648f-155">Если вы хотите присвоить новому фрагменту настраиваемое имя, просмотрите [фрагменты Rename](#rename-snippets) .</span><span class="sxs-lookup"><span data-stu-id="3648f-155">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="3648f-156">Редактирование фрагментов</span><span class="sxs-lookup"><span data-stu-id="3648f-156">Edit Snippets</span></span>   

1.  <span data-ttu-id="3648f-157">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="3648f-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="3648f-158">В области **фрагменты** щелкните имя фрагмента, который вы хотите изменить, чтобы открыть его в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="3648f-158">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  

    > ##### <span data-ttu-id="3648f-159">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="3648f-159">Figure 8</span></span>  
    > <span data-ttu-id="3648f-160">Редактор кода</span><span class="sxs-lookup"><span data-stu-id="3648f-160">The Code Editor</span></span>  
    > ![Редактор кода][ImageSnippetEditor]  

1.  <span data-ttu-id="3648f-162">С помощью **редактора кода** добавьте JavaScript в сниппет.</span><span class="sxs-lookup"><span data-stu-id="3648f-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="3648f-163">Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="3648f-163">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="3648f-164">Чтобы сохранить, нажмите клавиши `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3648f-164">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  

    > ##### <span data-ttu-id="3648f-165">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="3648f-165">Figure 9</span></span>  
    > <span data-ttu-id="3648f-166">Звездочка рядом с именем фрагмента, обозначающее несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="3648f-166">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    > ![Звездочка рядом с именем фрагмента, обозначающее несохраненный код.][ImageUnsavedSnippet]  

## <span data-ttu-id="3648f-168">Выполнение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="3648f-168">Run Snippets</span></span>   

### <span data-ttu-id="3648f-169">Выполнение фрагмента на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="3648f-169">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="3648f-170">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="3648f-170">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="3648f-171">Щелкните имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="3648f-171">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="3648f-172">Фрагмент откроется в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="3648f-172">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="3648f-173">Выберите команду **выполнить** фрагмент. ![ запустите фрагмент ][ImageRunSnippetIcon] или нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3648f-173">Click **Run Snippet** ![Run Snippet][ImageRunSnippetIcon], or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  

### <span data-ttu-id="3648f-174">Выполнение фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="3648f-174">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="3648f-175">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3648f-175">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="3648f-176">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3648f-176">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="3648f-177">Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="3648f-177">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  

    > ##### <span data-ttu-id="3648f-178">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="3648f-178">Figure 10</span></span>  
    > <span data-ttu-id="3648f-179">Выполнение фрагмента из меню команд</span><span class="sxs-lookup"><span data-stu-id="3648f-179">Running a Snippet from the Command Menu</span></span>  
    > ![Выполнение фрагмента из меню команд][ImageRunSnippetCommand]  

1.  <span data-ttu-id="3648f-181">Нажмите, `Enter` чтобы запустить фрагмент.</span><span class="sxs-lookup"><span data-stu-id="3648f-181">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="3648f-182">Переименование фрагментов</span><span class="sxs-lookup"><span data-stu-id="3648f-182">Rename Snippets</span></span>   

1.  <span data-ttu-id="3648f-183">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="3648f-183">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="3648f-184">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="3648f-184">Right-click the Snippet name and select **Rename**.</span></span>  

## <span data-ttu-id="3648f-185">Удаление фрагментов</span><span class="sxs-lookup"><span data-stu-id="3648f-185">Delete Snippets</span></span>   

1.  <span data-ttu-id="3648f-186">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="3648f-186">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="3648f-187">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="3648f-187">Right-click the Snippet name and select **Remove**.</span></span>  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "На рисунке 1 показано, как выглядит страница перед выполнением фрагмента."  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Рисунок 2: вид страницы после выполнения фрагмента."  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Рисунок 3: область фрагментов"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Рисунок 4: панель «источники» с открытой областью страниц в левой части экрана"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Рисунок 5: команда «Показать фрагменты»"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Рисунок 6: именование фрагмента"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Рисунок 7: команда для создания нового фрагмента кода"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Рисунок 8: редактор кода"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Рисунок 9: звездочка рядом с именем фрагмента, указывающая на несохраненный код."  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Рисунок 10: запуск фрагмента из меню команд"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли"  
[DevToolsSourcesPanel]: ../sources.md "Обзор палитры «источники»"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Пометок | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Кнопка-«Википедии»"  

> [!NOTE]
> <span data-ttu-id="3648f-202">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3648f-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3648f-203">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3648f-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3648f-205">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3648f-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Фрагменты — это небольшие сценарии, которые можно создавать и запускать на панели «источники» в Microsoft Edge DevTools.  Вы можете получать доступ к ним и запускать их на любой странице.  При запуске фрагмента кода выполняется из контекста открытой на данный момент страницы.
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5f6284179aacb471116a2d732507b010c37ef235
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993389"
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





# <span data-ttu-id="237c9-106">Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="237c9-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="237c9-107">Если вы обнаружите, что один и тот же код запускается повторно на [консоли][DevtoolsConsoleIndex] , попробуйте сохранить его как фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="237c9-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="237c9-108">Фрагменты — это сценарии, созданные вами на панели « [источники][DevToolsSourcesPanel] ».</span><span class="sxs-lookup"><span data-stu-id="237c9-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="237c9-109">У них есть доступ к контексту JavaScript на странице, и вы можете запускать их на любой странице.</span><span class="sxs-lookup"><span data-stu-id="237c9-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="237c9-110">Фрагменты — это альтернатива для [Закладка][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="237c9-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="237c9-111">В Firefox DevTools есть функция, похожая на фрагменты, которые называются [блокнотом][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="237c9-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="237c9-112">Например, на приведенном ниже рисунке показана домашняя страница DevTools слева и фрагмент исходного кода справа.</span><span class="sxs-lookup"><span data-stu-id="237c9-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="237c9-114">Вид страницы перед выполнением фрагмента</span><span class="sxs-lookup"><span data-stu-id="237c9-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="237c9-115">Исходный код фрагмента на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="237c9-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="237c9-116">На рисунке ниже показана страница после выполнения фрагмента.</span><span class="sxs-lookup"><span data-stu-id="237c9-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="237c9-117">Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое страницы полностью меняются.</span><span class="sxs-lookup"><span data-stu-id="237c9-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Вид страницы после выполнения фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="237c9-119">Вид страницы после выполнения фрагмента</span><span class="sxs-lookup"><span data-stu-id="237c9-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="237c9-120">Открытие области "фрагменты кода"</span><span class="sxs-lookup"><span data-stu-id="237c9-120">Open the Snippets pane</span></span>   

<span data-ttu-id="237c9-121">На панели **фрагментов** перечислены ваши фрагменты.</span><span class="sxs-lookup"><span data-stu-id="237c9-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="237c9-122">Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .</span><span class="sxs-lookup"><span data-stu-id="237c9-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Область фрагментов" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="237c9-124">Область **фрагментов**</span><span class="sxs-lookup"><span data-stu-id="237c9-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="237c9-125">Открытие области фрагментов с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="237c9-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="237c9-126">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="237c9-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="237c9-127">Обычно область **страницы** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="237c9-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Панель «источники» с открытой областью страницы в левой части экрана" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="237c9-129">Панель « **источники** » с открытой областью **страницы** в левой части экрана</span><span class="sxs-lookup"><span data-stu-id="237c9-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="237c9-130">Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .</span><span class="sxs-lookup"><span data-stu-id="237c9-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="237c9-131">**More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться нажать кнопку Другие вкладки \ (другие вкладки \).</span><span class="sxs-lookup"><span data-stu-id="237c9-131">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="237c9-132">Открытие области фрагментов с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="237c9-132">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="237c9-133">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="237c9-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="237c9-134">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="237c9-134">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="237c9-135">Начните вводить текст `Snippets` , нажмите кнопку **Показать фрагменты**и нажмите клавишу `Enter` для запуска команды.</span><span class="sxs-lookup"><span data-stu-id="237c9-135">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда «Показать фрагменты»" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="237c9-137">Команда « **Показать фрагменты** »</span><span class="sxs-lookup"><span data-stu-id="237c9-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="237c9-138">Создание фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="237c9-138">Create Snippets</span></span>   

### <span data-ttu-id="237c9-139">Создание фрагмента с помощью панели «источники»</span><span class="sxs-lookup"><span data-stu-id="237c9-139">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="237c9-140">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="237c9-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="237c9-141">Нажмите кнопку **создать фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="237c9-141">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="237c9-142">Введите имя для фрагмента, а затем нажмите `Enter` для сохранения.</span><span class="sxs-lookup"><span data-stu-id="237c9-142">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Присвоение имени фрагменту" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="237c9-144">Присвоение имени фрагменту</span><span class="sxs-lookup"><span data-stu-id="237c9-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="237c9-145">Создание фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="237c9-145">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="237c9-146">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="237c9-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="237c9-147">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="237c9-147">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="237c9-148">Начните вводить текст `Snippet` , выберите **создать новый фрагмент**, а затем нажмите, `Enter` чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="237c9-148">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда для создания нового фрагмента." lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="237c9-150">Команда для создания нового фрагмента.</span><span class="sxs-lookup"><span data-stu-id="237c9-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="237c9-151">Если вы хотите присвоить новому фрагменту настраиваемое имя, просмотрите [фрагменты Rename](#rename-snippets) .</span><span class="sxs-lookup"><span data-stu-id="237c9-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="237c9-152">Редактирование фрагментов</span><span class="sxs-lookup"><span data-stu-id="237c9-152">Edit Snippets</span></span>   

1.  <span data-ttu-id="237c9-153">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="237c9-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="237c9-154">В области **фрагменты** щелкните имя фрагмента, который вы хотите изменить, чтобы открыть его в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="237c9-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="237c9-156">**Редактор кода**</span><span class="sxs-lookup"><span data-stu-id="237c9-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="237c9-157">С помощью **редактора кода** добавьте JavaScript в сниппет.</span><span class="sxs-lookup"><span data-stu-id="237c9-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="237c9-158">Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="237c9-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="237c9-159">Чтобы сохранить, нажмите клавиши `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="237c9-159">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента, обозначающее несохраненный код." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="237c9-161">Звездочка рядом с именем фрагмента, обозначающее несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="237c9-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="237c9-162">Выполнение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="237c9-162">Run Snippets</span></span>   

### <span data-ttu-id="237c9-163">Выполнение фрагмента на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="237c9-163">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="237c9-164">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="237c9-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="237c9-165">Щелкните имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="237c9-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="237c9-166">Фрагмент откроется в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="237c9-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="237c9-167">Выберите команду **выполнить фрагмент** \ ( ![ выполнить фрагмент \ ][ImageRunSnippetIcon] ) или нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="237c9-167">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="237c9-168">Выполнение фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="237c9-168">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="237c9-169">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="237c9-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="237c9-170">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="237c9-170">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="237c9-171">Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="237c9-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Выполнение фрагмента из меню команд" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="237c9-173">Выполнение фрагмента из **меню команд**</span><span class="sxs-lookup"><span data-stu-id="237c9-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="237c9-174">Нажмите, `Enter` чтобы запустить фрагмент.</span><span class="sxs-lookup"><span data-stu-id="237c9-174">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="237c9-175">Переименование фрагментов</span><span class="sxs-lookup"><span data-stu-id="237c9-175">Rename Snippets</span></span>   

1.  <span data-ttu-id="237c9-176">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="237c9-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="237c9-177">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="237c9-177">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="237c9-178">Удаление фрагментов</span><span class="sxs-lookup"><span data-stu-id="237c9-178">Delete Snippets</span></span>   

1.  <span data-ttu-id="237c9-179">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="237c9-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="237c9-180">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="237c9-180">Right-click the Snippet name and select **Remove**.</span></span>  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Обзор панели «источники» | Документы Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Пометок | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Кнопка-«Википедии»"  

> [!NOTE]
> <span data-ttu-id="237c9-185">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="237c9-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="237c9-186">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="237c9-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="237c9-188">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="237c9-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

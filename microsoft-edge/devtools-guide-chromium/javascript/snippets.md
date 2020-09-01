---
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3a5ae986e3080a0b6a8b1bf34b0e0efc44c90303
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982033"
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





# <span data-ttu-id="18447-103">Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="18447-103">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="18447-104">Если вы обнаружите, что один и тот же код запускается повторно на [консоли][DevtoolsConsoleIndex] , попробуйте сохранить его как фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="18447-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="18447-105">Фрагменты — это сценарии, созданные вами на панели « [источники][DevToolsSourcesPanel] ».</span><span class="sxs-lookup"><span data-stu-id="18447-105">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="18447-106">У них есть доступ к контексту JavaScript на странице, и вы можете запускать их на любой странице.</span><span class="sxs-lookup"><span data-stu-id="18447-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="18447-107">Фрагменты — это альтернатива для [Закладка][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="18447-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="18447-108">В Firefox DevTools есть функция, похожая на фрагменты, которые называются [блокнотом][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="18447-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="18447-109">Например, на приведенном ниже рисунке показана домашняя страница DevTools слева и фрагмент исходного кода справа.</span><span class="sxs-lookup"><span data-stu-id="18447-109">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="18447-111">Вид страницы перед выполнением фрагмента</span><span class="sxs-lookup"><span data-stu-id="18447-111">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="18447-112">Исходный код фрагмента на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="18447-112">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="18447-113">На рисунке ниже показана страница после выполнения фрагмента.</span><span class="sxs-lookup"><span data-stu-id="18447-113">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="18447-114">Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое страницы полностью меняются.</span><span class="sxs-lookup"><span data-stu-id="18447-114">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Вид страницы после выполнения фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="18447-116">Вид страницы после выполнения фрагмента</span><span class="sxs-lookup"><span data-stu-id="18447-116">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="18447-117">Открытие области "фрагменты кода"</span><span class="sxs-lookup"><span data-stu-id="18447-117">Open the Snippets pane</span></span>   

<span data-ttu-id="18447-118">На панели **фрагментов** перечислены ваши фрагменты.</span><span class="sxs-lookup"><span data-stu-id="18447-118">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="18447-119">Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .</span><span class="sxs-lookup"><span data-stu-id="18447-119">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Область фрагментов" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="18447-121">Область **фрагментов**</span><span class="sxs-lookup"><span data-stu-id="18447-121">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="18447-122">Открытие области фрагментов с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="18447-122">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="18447-123">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="18447-123">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="18447-124">Обычно область **страницы** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18447-124">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Панель «источники» с открытой областью страницы в левой части экрана" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="18447-126">Панель « **источники** » с открытой областью **страницы** в левой части экрана</span><span class="sxs-lookup"><span data-stu-id="18447-126">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18447-127">Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .</span><span class="sxs-lookup"><span data-stu-id="18447-127">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="18447-128">**More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться нажать кнопку Другие вкладки \ (другие вкладки \).</span><span class="sxs-lookup"><span data-stu-id="18447-128">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="18447-129">Открытие области фрагментов с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="18447-129">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="18447-130">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="18447-130">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="18447-131">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="18447-131">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="18447-132">Начните вводить текст `Snippets` , нажмите кнопку **Показать фрагменты**и нажмите клавишу `Enter` для запуска команды.</span><span class="sxs-lookup"><span data-stu-id="18447-132">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда «Показать фрагменты»" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="18447-134">Команда « **Показать фрагменты** »</span><span class="sxs-lookup"><span data-stu-id="18447-134">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="18447-135">Создание фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="18447-135">Create Snippets</span></span>   

### <span data-ttu-id="18447-136">Создание фрагмента с помощью панели «источники»</span><span class="sxs-lookup"><span data-stu-id="18447-136">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="18447-137">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="18447-137">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="18447-138">Нажмите кнопку **создать фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="18447-138">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="18447-139">Введите имя для фрагмента, а затем нажмите `Enter` для сохранения.</span><span class="sxs-lookup"><span data-stu-id="18447-139">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Присвоение имени фрагменту" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="18447-141">Присвоение имени фрагменту</span><span class="sxs-lookup"><span data-stu-id="18447-141">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="18447-142">Создание фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="18447-142">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="18447-143">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="18447-143">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="18447-144">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="18447-144">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="18447-145">Начните вводить текст `Snippet` , выберите **создать новый фрагмент**, а затем нажмите, `Enter` чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="18447-145">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда для создания нового фрагмента." lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="18447-147">Команда для создания нового фрагмента.</span><span class="sxs-lookup"><span data-stu-id="18447-147">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="18447-148">Если вы хотите присвоить новому фрагменту настраиваемое имя, просмотрите [фрагменты Rename](#rename-snippets) .</span><span class="sxs-lookup"><span data-stu-id="18447-148">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="18447-149">Редактирование фрагментов</span><span class="sxs-lookup"><span data-stu-id="18447-149">Edit Snippets</span></span>   

1.  <span data-ttu-id="18447-150">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="18447-150">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="18447-151">В области **фрагменты** щелкните имя фрагмента, который вы хотите изменить, чтобы открыть его в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="18447-151">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="18447-153">**Редактор кода**</span><span class="sxs-lookup"><span data-stu-id="18447-153">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18447-154">С помощью **редактора кода** добавьте JavaScript в сниппет.</span><span class="sxs-lookup"><span data-stu-id="18447-154">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="18447-155">Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="18447-155">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="18447-156">Чтобы сохранить, нажмите клавиши `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="18447-156">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента, обозначающее несохраненный код." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="18447-158">Звездочка рядом с именем фрагмента, обозначающее несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="18447-158">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="18447-159">Выполнение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="18447-159">Run Snippets</span></span>   

### <span data-ttu-id="18447-160">Выполнение фрагмента на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="18447-160">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="18447-161">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="18447-161">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="18447-162">Щелкните имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="18447-162">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="18447-163">Фрагмент откроется в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="18447-163">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="18447-164">Выберите команду **выполнить фрагмент** \ ( ![ выполнить фрагмент \ ][ImageRunSnippetIcon] ) или нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="18447-164">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="18447-165">Выполнение фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="18447-165">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="18447-166">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="18447-166">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="18447-167">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="18447-167">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="18447-168">Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="18447-168">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Выполнение фрагмента из меню команд" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="18447-170">Выполнение фрагмента из **меню команд**</span><span class="sxs-lookup"><span data-stu-id="18447-170">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="18447-171">Нажмите, `Enter` чтобы запустить фрагмент.</span><span class="sxs-lookup"><span data-stu-id="18447-171">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="18447-172">Переименование фрагментов</span><span class="sxs-lookup"><span data-stu-id="18447-172">Rename Snippets</span></span>   

1.  <span data-ttu-id="18447-173">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="18447-173">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="18447-174">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="18447-174">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="18447-175">Удаление фрагментов</span><span class="sxs-lookup"><span data-stu-id="18447-175">Delete Snippets</span></span>   

1.  <span data-ttu-id="18447-176">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="18447-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="18447-177">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="18447-177">Right-click the Snippet name and select **Remove**.</span></span>  
    
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
> <span data-ttu-id="18447-182">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18447-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="18447-183">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="18447-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="18447-185">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18447-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

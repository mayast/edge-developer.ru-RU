---
title: Просмотр ресурсов страницы с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611919"
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





# <span data-ttu-id="cfe52-103">Просмотр ресурсов страницы с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cfe52-103">View Page Resources With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="cfe52-104">В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="cfe52-104">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="cfe52-105">Ресурсы — это файлы, необходимые для правильного отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="cfe52-105">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="cfe52-106">Примеры ресурсов включают CSS, JavaScript и HTML-файлы, а также изображения.</span><span class="sxs-lookup"><span data-stu-id="cfe52-106">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="cfe52-107">В этом руководстве предполагается, что вы знакомы с основами [веб-разработки][MDNLearnWebDevelopment] и [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="cfe52-107">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="cfe52-108">Открытие ресурсов</span><span class="sxs-lookup"><span data-stu-id="cfe52-108">Open resources</span></span>   

<span data-ttu-id="cfe52-109">Если вы знаете имя ресурса, который вы хотите проверить, **меню команд** предоставляет быстрый способ открытия ресурса.</span><span class="sxs-lookup"><span data-stu-id="cfe52-109">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="cfe52-110">Нажмите клавиши `Control` + `P` \ (Windows \) или `Command` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="cfe52-110">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="cfe52-111">Откроется диалоговое окно **Открытие файла** .</span><span class="sxs-lookup"><span data-stu-id="cfe52-111">The **Open File** dialog opens.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-112">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="cfe52-112">Figure 1</span></span>  
    > <span data-ttu-id="cfe52-113">Диалоговое окно « **Открытие файла** »</span><span class="sxs-lookup"><span data-stu-id="cfe52-113">The **Open File** dialog</span></span>  
    > ![Диалоговое окно «Открытие файла»][ImageOpenFile]  
    
1.  <span data-ttu-id="cfe52-115">Выберите файл из раскрывающегося списка или введите имя файла и нажмите `Enter` один раз, чтобы выделить его в поле "Автозаполнение".</span><span class="sxs-lookup"><span data-stu-id="cfe52-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-116">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="cfe52-116">Figure 2</span></span>  
    > <span data-ttu-id="cfe52-117">Ввод имени файла в диалоговом окне " **Открытие файла** "</span><span class="sxs-lookup"><span data-stu-id="cfe52-117">Typing a filename in the **Open File** dialog</span></span>  
    > ![Ввод имени файла в диалоговом окне "Открытие файла"][ImageFileSearch]  
    
### <span data-ttu-id="cfe52-119">Открытие ресурсов на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="cfe52-119">Open resources in the Network panel</span></span>   

<span data-ttu-id="cfe52-120">Ознакомьтесь [с подробными сведениями о ресурсе][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="cfe52-120">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

> ##### <span data-ttu-id="cfe52-121">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="cfe52-121">Figure 3</span></span>  
> <span data-ttu-id="cfe52-122">Проверка ресурса на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="cfe52-122">Inspecting a resource in the Network panel</span></span>  
> ![Проверка ресурса на панели "сеть"][ImageNetworkResponse]  

### <span data-ttu-id="cfe52-124">Показать ресурсы на панели "сеть" с других панелей</span><span class="sxs-lookup"><span data-stu-id="cfe52-124">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="cfe52-125">В разделе [Обзор ресурсов](#browse-resources) ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.</span><span class="sxs-lookup"><span data-stu-id="cfe52-125">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="cfe52-126">Если вы когда-нибудь хотите просмотреть ресурс на панели **сеть** , щелкните ресурс правой кнопкой мыши и выберите пункт **Показать на панели "сеть**".</span><span class="sxs-lookup"><span data-stu-id="cfe52-126">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

> ##### <span data-ttu-id="cfe52-127">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="cfe52-127">Figure 4</span></span>  
> <span data-ttu-id="cfe52-128">Параметр « **Показать в сети»**</span><span class="sxs-lookup"><span data-stu-id="cfe52-128">The **Reveal in Network panel** option</span></span>  
> ![Панель "Показать в сети"][ImageRevealNetwork]  

## <span data-ttu-id="cfe52-130">Просмотр ресурсов</span><span class="sxs-lookup"><span data-stu-id="cfe52-130">Browse resources</span></span>   

### <span data-ttu-id="cfe52-131">Просмотр ресурсов на панели «Сеть»</span><span class="sxs-lookup"><span data-stu-id="cfe52-131">Browse resources in the Network panel</span></span>   

<span data-ttu-id="cfe52-132">Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="cfe52-132">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

> ##### <span data-ttu-id="cfe52-133">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="cfe52-133">Figure 5</span></span>  
> <span data-ttu-id="cfe52-134">Ресурсы страницы в журнале сети</span><span class="sxs-lookup"><span data-stu-id="cfe52-134">Page resources in the Network Log</span></span>  
> ![Ресурсы страницы в журнале сети][ImageNetworkLog]  

### <span data-ttu-id="cfe52-136">Просмотр по каталогу</span><span class="sxs-lookup"><span data-stu-id="cfe52-136">Browse by directory</span></span>   

<span data-ttu-id="cfe52-137">Чтобы просмотреть ресурсы на странице, упорядоченные по каталогу, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cfe52-137">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="cfe52-138">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="cfe52-138">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="cfe52-139">Щелкните вкладку **страницы** , чтобы показать ресурсы страницы.</span><span class="sxs-lookup"><span data-stu-id="cfe52-139">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="cfe52-140">Откроется область **страница** .</span><span class="sxs-lookup"><span data-stu-id="cfe52-140">The **Page** pane opens.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-141">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="cfe52-141">Figure 6</span></span>  
    > <span data-ttu-id="cfe52-142">Область **страницы**</span><span class="sxs-lookup"><span data-stu-id="cfe52-142">The **Page** pane</span></span>  
    > ![Область страницы][ImagePage]  
    
    <span data-ttu-id="cfe52-144">Ниже приведено разделение элементов, не являющихся очевидными, на [рисунке 6](#figure-6).</span><span class="sxs-lookup"><span data-stu-id="cfe52-144">Here is a breakdown of the non-obvious items in [Figure 6](#figure-6):</span></span>  
    
    | <span data-ttu-id="cfe52-145">Элемент страницы</span><span class="sxs-lookup"><span data-stu-id="cfe52-145">Page item</span></span> | <span data-ttu-id="cfe52-146">Описание</span><span class="sxs-lookup"><span data-stu-id="cfe52-146">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="cfe52-147">Основной [контекст обзора][MDNInlineFrame]документов.</span><span class="sxs-lookup"><span data-stu-id="cfe52-147">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="cfe52-148">Домен.</span><span class="sxs-lookup"><span data-stu-id="cfe52-148">The domain.</span></span>  <span data-ttu-id="cfe52-149">Все ресурсы, вложенные в него, поступают из этого домена.</span><span class="sxs-lookup"><span data-stu-id="cfe52-149">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="cfe52-150">Например, может быть задан полный URL-адрес `comlink.global.j` файла `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="cfe52-150">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="cfe52-151">Каталог.</span><span class="sxs-lookup"><span data-stu-id="cfe52-151">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="cfe52-152">Основной HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="cfe52-152">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="cfe52-153">Контекст среды выполнения рабочего процесса службы.</span><span class="sxs-lookup"><span data-stu-id="cfe52-153">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="cfe52-154">Щелкните ресурс, чтобы просмотреть его в **редакторе**.</span><span class="sxs-lookup"><span data-stu-id="cfe52-154">Click a resource to view it in the **Editor**.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-155">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="cfe52-155">Figure 7</span></span>  
    > <span data-ttu-id="cfe52-156">Просмотр файла в **редакторе**</span><span class="sxs-lookup"><span data-stu-id="cfe52-156">Viewing a file in the **Editor**</span></span>  
    > ![Просмотр файла в редакторе][ImageSourcesView]  
    
### <span data-ttu-id="cfe52-158">Просмотр по имени файла</span><span class="sxs-lookup"><span data-stu-id="cfe52-158">Browse by filename</span></span>   

<span data-ttu-id="cfe52-159">По умолчанию в области **страницы** ресурсы группируются по каталогам.</span><span class="sxs-lookup"><span data-stu-id="cfe52-159">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="cfe52-160">Чтобы отключить эту группировку и просмотреть ресурсы для каждого домена в виде плоского списка, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cfe52-160">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="cfe52-161">Открытие области **страницы** .</span><span class="sxs-lookup"><span data-stu-id="cfe52-161">Open the **Page** pane.</span></span>  <span data-ttu-id="cfe52-162">Просмотр [по каталогу](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="cfe52-162">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="cfe52-163">Нажмите кнопку **Дополнительные параметры** `...` и отключите функцию **Группировка по папкам**.</span><span class="sxs-lookup"><span data-stu-id="cfe52-163">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-164">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="cfe52-164">Figure 8</span></span>  
    > <span data-ttu-id="cfe52-165">Параметр **Группировка по папке**</span><span class="sxs-lookup"><span data-stu-id="cfe52-165">The **Group By Folder** option</span></span>  
    > ![Параметр Группировка по папке][ImageGroupByFolder]  
    
    <span data-ttu-id="cfe52-167">Ресурсы упорядочены по типам файлов.</span><span class="sxs-lookup"><span data-stu-id="cfe52-167">Resources are organized by file type.</span></span>  <span data-ttu-id="cfe52-168">В каждом типе файла ресурсы упорядочены по алфавиту.</span><span class="sxs-lookup"><span data-stu-id="cfe52-168">Within each file type the resources are organized alphabetically.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-169">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="cfe52-169">Figure 9</span></span>  
    > <span data-ttu-id="cfe52-170">Область **страницы** после отключения **группировки по папке**</span><span class="sxs-lookup"><span data-stu-id="cfe52-170">The **Page** pane after disabling **Group By Folder**</span></span>  
    > ![Область страницы после отключения группировки по папке][ImageFileNames]  
    
### <span data-ttu-id="cfe52-172">Просмотр по типу файла</span><span class="sxs-lookup"><span data-stu-id="cfe52-172">Browse by file type</span></span>   

<span data-ttu-id="cfe52-173">Чтобы сгруппировать ресурсы в зависимости от типа файла:</span><span class="sxs-lookup"><span data-stu-id="cfe52-173">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="cfe52-174">Откройте вкладку **приложение** .  Откроется панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="cfe52-174">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="cfe52-175">По умолчанию область **манифеста** обычно открывается в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="cfe52-175">By default the **Manifest** pane usually opens first.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-176">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="cfe52-176">Figure 10</span></span>  
    > <span data-ttu-id="cfe52-177">Панель **приложения**</span><span class="sxs-lookup"><span data-stu-id="cfe52-177">The **Application** panel</span></span>  
    > ![Панель приложения][ImageApplication]  
    
1.  <span data-ttu-id="cfe52-179">Прокрутите страницу вниз до области **рамок** .</span><span class="sxs-lookup"><span data-stu-id="cfe52-179">Scroll down to the **Frames** pane.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-180">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="cfe52-180">Figure 11</span></span>  
    > <span data-ttu-id="cfe52-181">Область **рамок**</span><span class="sxs-lookup"><span data-stu-id="cfe52-181">The **Frames** pane</span></span>  
    > ![Область рамок][ImageFrames]  
    
1.  <span data-ttu-id="cfe52-183">Разверните разделы, в которых вы заинтересованы.</span><span class="sxs-lookup"><span data-stu-id="cfe52-183">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="cfe52-184">Щелкните ресурс, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="cfe52-184">Click a resource to view it.</span></span>  
    
    > ##### <span data-ttu-id="cfe52-185">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="cfe52-185">Figure 12</span></span>  
    > <span data-ttu-id="cfe52-186">Просмотр ресурса на панели « **приложение** »</span><span class="sxs-lookup"><span data-stu-id="cfe52-186">Viewing a resource in the **Application** panel</span></span>  
    > ![Просмотр ресурса на панели «приложение»][ImageApplicationView]  

#### <span data-ttu-id="cfe52-188">Просмотр файлов по типу на панели «Сеть»</span><span class="sxs-lookup"><span data-stu-id="cfe52-188">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="cfe52-189">Просмотреть [Фильтр по типу ресурсов][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="cfe52-189">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

> ##### <span data-ttu-id="cfe52-190">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="cfe52-190">Figure 13</span></span>  
> <span data-ttu-id="cfe52-191">Фильтрация для CSS в сетевом журнале</span><span class="sxs-lookup"><span data-stu-id="cfe52-191">Filtering for CSS in the Network Log</span></span>  
> ![Фильтрация для CSS в сетевом журнале][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Рисунок 1: диалоговое окно "открыть файл""  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Рисунок 2: ввод имени файла в диалоговом окне "Открытие файла""  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Рисунок 3: Проверка ресурса на панели * * Network * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Рисунок 4: Показать на панели "сеть""  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Рисунок 5: ресурсы страницы в журнале сети"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Рисунок 6: область страницы"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Рис. 7: Просмотр файла в редакторе"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Рисунок 8: параметр группировка по папке"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Рисунок 9: область страницы после отключения группы по папке"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Рисунок 10: панель приложения"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Рисунок 11: область рамок"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Рисунок 12: Просмотр ресурса на панели «приложение»"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Рисунок 13: Фильтрация CSS в сетевом журнале"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Фильтрация по типу ресурсов: Проверка активности сети в Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Просмотрите сведения об активности в сети для проверки ресурсов в Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Регистрация активности сети — проверка активности сети в Microsoft Edge DevTools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> IFRAME: элемент встроенной рамки | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Знакомство с веб-разработкой | MDN"  

> [!NOTE]
> <span data-ttu-id="cfe52-212">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cfe52-212">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cfe52-213">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/resources/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="cfe52-213">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cfe52-215">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cfe52-215">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

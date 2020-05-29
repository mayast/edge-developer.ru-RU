---
title: Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 659120414597273b15657377c33c800e0c83b7cb
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601840"
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





# <span data-ttu-id="c812f-103">Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)</span><span class="sxs-lookup"><span data-stu-id="c812f-103">Force Microsoft Edge DevTools Into Print Preview Mode (CSS Print Media Type)</span></span>   



<span data-ttu-id="c812f-104">[Запрос на печать][MDNUsingMediaQueries] позволяет управлять тем, как выглядит страница после печати.</span><span class="sxs-lookup"><span data-stu-id="c812f-104">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="c812f-105">Чтобы перевести страницу в режим предварительного просмотра, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c812f-105">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="c812f-106">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="c812f-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="c812f-107">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="c812f-107">Figure 1</span></span>  
    > <span data-ttu-id="c812f-108">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="c812f-108">The **Command Menu**</span></span>  
    > ![Меню команд][ImageCommandMenu]  
    
1.  <span data-ttu-id="c812f-110">Введите `rendering` команду **Показать рендеринг**и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c812f-110">Type `rendering`, select **Show Rendering**, and then press `Enter`.</span></span>  
1.  <span data-ttu-id="c812f-111">В разделе **Эмуляция мультимедиа в CSS** выберите **Печать**.</span><span class="sxs-lookup"><span data-stu-id="c812f-111">Under **Emulate CSS media** select **print**.</span></span>  
    
    > ##### <span data-ttu-id="c812f-112">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="c812f-112">Figure 2</span></span>  
    > <span data-ttu-id="c812f-113">Режим предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="c812f-113">Print preview mode</span></span>  
    > ![Режим предварительного просмотра][ImagePrintMode]  
    
<span data-ttu-id="c812f-115">Отсюда вы можете просматривать и изменять CSS, как и любую другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="c812f-115">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="c812f-116">Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="c812f-116">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

 



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Рисунок 1: меню команд"  
[ImagePrintMode]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png "Рисунок 2: режим предварительного просмотра"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование мультимедийных запросов | MDN"  

> [!NOTE]
> <span data-ttu-id="c812f-122">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c812f-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c812f-123">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c812f-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c812f-125">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c812f-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

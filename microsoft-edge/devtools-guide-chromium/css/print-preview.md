---
description: Откройте вкладку "рендеринг" и выберите "Эмуляция CSS Media" > "Печать".
title: Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1b71135c5ed2d86903b76e659434ee2125985a24
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993053"
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





# <span data-ttu-id="8063c-104">Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)</span><span class="sxs-lookup"><span data-stu-id="8063c-104">Force Microsoft Edge DevTools into Print Preview mode (CSS Print Media Type)</span></span>   



<span data-ttu-id="8063c-105">[Запрос на печать][MDNUsingMediaQueries] позволяет управлять тем, как выглядит страница после печати.</span><span class="sxs-lookup"><span data-stu-id="8063c-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="8063c-106">Чтобы перевести страницу в режим предварительного просмотра, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8063c-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="8063c-107">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="8063c-107">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="8063c-109">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="8063c-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8063c-110">Введите `rendering` команду **Показать рендеринг**и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="8063c-110">Type `rendering`, select **Show Rendering**, and then press `Enter`.</span></span>  
1.  <span data-ttu-id="8063c-111">В разделе **Эмуляция мультимедиа в CSS** выберите **Печать**.</span><span class="sxs-lookup"><span data-stu-id="8063c-111">Under **Emulate CSS media** select **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Режим предварительного просмотра" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="8063c-113">Режим предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="8063c-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="8063c-114">Отсюда вы можете просматривать и изменять CSS, как и любую другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="8063c-114">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="8063c-115">Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="8063c-115">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevToolsCSSGetStarted]: ./index.md "Начало просмотра и изменения CSS | Документы Microsoft"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование мультимедийных запросов | MDN"  

> [!NOTE]
> <span data-ttu-id="8063c-119">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8063c-119">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8063c-120">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="8063c-120">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8063c-122">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8063c-122">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

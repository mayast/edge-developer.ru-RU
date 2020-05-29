---
title: Помечайте сценарии содержимого как код библиотеки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: fe34d8f2fb656283b1821441162b93d47d51d24e
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581791"
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





# <span data-ttu-id="d0b7d-103">Помечайте сценарии содержимого как код библиотеки</span><span class="sxs-lookup"><span data-stu-id="d0b7d-103">Mark Content Scripts as Library Code</span></span>   



<span data-ttu-id="d0b7d-104">При использовании панели **Sources (источники** данных) Microsoft Edge DevTools для [перехода по коду][DevToolsJavascriptStepThroughCode], иногда наведите указатель мыши на код, который вы не знаете.</span><span class="sxs-lookup"><span data-stu-id="d0b7d-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="d0b7d-105">Возможно, вы приостановили код для одного из установленных расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d0b7d-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="d0b7d-106">Выполните указанные ниже действия, чтобы не приостанавливаться на коде расширения.</span><span class="sxs-lookup"><span data-stu-id="d0b7d-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="d0b7d-107">Откройте DevTools, выберите пункт **Настройка DevTools и управление** `...` **параметрами**.</span><span class="sxs-lookup"><span data-stu-id="d0b7d-107">Open DevTools, select **Customize and control DevTools** `...` and click **Settings**.</span></span>  <span data-ttu-id="d0b7d-108">Вы также можете открыть **Параметры** , нажав клавишу `F1` .</span><span class="sxs-lookup"><span data-stu-id="d0b7d-108">You may also open **Settings** by pressing `F1`.</span></span>  

1.  <span data-ttu-id="d0b7d-109">Откройте вкладку **код библиотеки** , которая открывает раздел **код библиотеки Framework** **параметров**.</span><span class="sxs-lookup"><span data-stu-id="d0b7d-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="d0b7d-110">Установите флажок **помечать сценарии содержимого как библиотечный код** .</span><span class="sxs-lookup"><span data-stu-id="d0b7d-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="d0b7d-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="d0b7d-111">Figure 1</span></span>  
    > <span data-ttu-id="d0b7d-112">Флажок " **помечать сценарии содержимого как библиотеку кода** "</span><span class="sxs-lookup"><span data-stu-id="d0b7d-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    > ![Флажок "помечать сценарии содержимого как библиотеку кода"][ImageMarkContentScriptsLibraryCode]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMarkContentScriptsLibraryCode]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png "Рисунок 1: флажок "помечать сценарии содержимого как библиотеку кода""  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Шаг 4: пошаговое руководство по написанию кода — начало работы с отладкой JavaScript в Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="d0b7d-116">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0b7d-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d0b7d-117">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).</span><span class="sxs-lookup"><span data-stu-id="d0b7d-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d0b7d-119">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0b7d-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: Контроль значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 39a7967a7dd1d0b34eb802d2879e04a64afd0dd0
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982240"
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





# <span data-ttu-id="5ea01-103">Контроль значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе</span><span class="sxs-lookup"><span data-stu-id="5ea01-103">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="5ea01-104">Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.</span><span class="sxs-lookup"><span data-stu-id="5ea01-104">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="5ea01-105">С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.</span><span class="sxs-lookup"><span data-stu-id="5ea01-105">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="5ea01-106">Значение выражения обновляется почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="5ea01-106">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="5ea01-107">Создание выражения в реальном времени</span><span class="sxs-lookup"><span data-stu-id="5ea01-107">Create a Live Expression</span></span>   

1.  <span data-ttu-id="5ea01-108">[Открытие консоли][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="5ea01-108">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="5ea01-109">Щелкните **создать выражение в реальном времени** \ ( ![ создать выражение в реальном времени ][ImageCreateLiveExpressionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="5ea01-109">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="5ea01-110">Появится текстовое поле " **выражение в реальном времени** ".</span><span class="sxs-lookup"><span data-stu-id="5ea01-110">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Ввод данных Document. activeElement в текстовое поле "Интерактивное выражение"" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="5ea01-112">Ввод `document.activeElement` текста в текстовое поле " **интерактивное выражение** "</span><span class="sxs-lookup"><span data-stu-id="5ea01-112">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5ea01-113">Введите `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \), чтобы сохранить выражение, или щелкните любое место за пределами текстового поля **Live Expression** .</span><span class="sxs-lookup"><span data-stu-id="5ea01-113">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Открытие ссылки на консоль консоли | Документы Microsoft"  

> [!NOTE]
> <span data-ttu-id="5ea01-115">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5ea01-115">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5ea01-116">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5ea01-116">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5ea01-118">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5ea01-118">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

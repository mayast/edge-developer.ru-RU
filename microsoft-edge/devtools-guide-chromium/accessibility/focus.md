---
title: Отслеживание элемента, на который установлен фокус
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: a1bcb7e97357d1348b363ecd4842d1b6a78feb45
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581533"
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





# <span data-ttu-id="43a25-103">Отслеживание элемента, на который установлен фокус</span><span class="sxs-lookup"><span data-stu-id="43a25-103">Track Which Element Has Focus</span></span>   



<span data-ttu-id="43a25-104">Предположим, что вы тестируете специальные возможности навигации с помощью клавиатуры для страницы.</span><span class="sxs-lookup"><span data-stu-id="43a25-104">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="43a25-105">При переходе по странице с помощью `Tab` клавиши иногда теряется фокус, так как элемент, на который установлен фокус, скрыт.</span><span class="sxs-lookup"><span data-stu-id="43a25-105">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  <span data-ttu-id="43a25-106">Чтобы отследить фокусируемый элемент в DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="43a25-106">To track the focused element in DevTools:</span></span>  

1.  <span data-ttu-id="43a25-107">Открытие **консоли**.</span><span class="sxs-lookup"><span data-stu-id="43a25-107">Open the **Console**.</span></span>  
1.  <span data-ttu-id="43a25-108">Щелкните создать выражение для создания **динамического выражения** ![ ][ImageCreateIcon] .</span><span class="sxs-lookup"><span data-stu-id="43a25-108">Click **Create Live Expression** ![Create Live Expression][ImageCreateIcon].</span></span>  

    > ##### <span data-ttu-id="43a25-109">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="43a25-109">Figure 1</span></span>  
    > <span data-ttu-id="43a25-110">Создание **выражения в реальном времени**</span><span class="sxs-lookup"><span data-stu-id="43a25-110">Creating a **Live Expression**</span></span>  
    > ![Создание выражения в реальном времени][ImageLiveExpression]  
    
1.  <span data-ttu-id="43a25-112">Введите `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="43a25-112">Type `document.activeElement`.</span></span>
1.  <span data-ttu-id="43a25-113">Щелкните за пределами пользовательского интерфейса **Live Expression** , чтобы сохранить его.</span><span class="sxs-lookup"><span data-stu-id="43a25-113">Click outside of the **Live Expression** UI to save.</span></span>

<span data-ttu-id="43a25-114">Значение, которое вы видите ниже, `document.activeElement` является результатом выражения.</span><span class="sxs-lookup"><span data-stu-id="43a25-114">The value that you see below `document.activeElement` is the result of the expression.</span></span>  
<span data-ttu-id="43a25-115">Так как это выражение всегда представляет фокусируемый элемент, вы можете всегда следить за тем, какой элемент находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="43a25-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="43a25-116">Наведите указатель мыши на результат, чтобы выделиь фокусируемый элемент в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="43a25-116">Hover over the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="43a25-117">Щелкните результат правой кнопкой мыши и выберите пункт **Показать на панели элементов** , чтобы отобразить элемент в дереве DOM на панели **элементы** .</span><span class="sxs-lookup"><span data-stu-id="43a25-117">Right-click the result and select **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** panel.</span></span>  
*   <span data-ttu-id="43a25-118">Щелкните результат правой кнопкой мыши и выберите **Сохранить как глобальную переменную** , чтобы создать ссылку на переменную на узел, который вы можете использовать на **консоли**.</span><span class="sxs-lookup"><span data-stu-id="43a25-118">Right-click the result and select **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCreateIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpression]: /microsoft-edge/devtools-guide-chromium/media/accessibility-console-create-live-expression-empty.msft.png "Рисунок 1: создание выражения в реальном времени"  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="43a25-120">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43a25-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="43a25-121">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).</span><span class="sxs-lookup"><span data-stu-id="43a25-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="43a25-123">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43a25-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

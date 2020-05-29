---
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
description: Сведения о том, как создавать, проектировать и тестировать веб-сайты со специальными возможностями в Microsoft Edge.
title: Специальные возможности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Специальные возможности, Специальные возможности для разработчиков, доступные веб-сайты, EDGE, веб-разработка, ARIA, разработчик, модель автоматизации пользовательского интерфейса
ms.openlocfilehash: 6ad95e9c250aa6a4a61ca09470cea86efd715427
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583107"
---
# <span data-ttu-id="2330c-104">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="2330c-104">Accessibility</span></span>  

> <span data-ttu-id="2330c-105">"\ [T \] его влияние на световые возможности радикально изменилось в Интернете, так как в Интернете удаляются барьеры для общения и взаимодействия, которые многие люди сталкиваются с физическим миром."</span><span class="sxs-lookup"><span data-stu-id="2330c-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="2330c-106">(Специальные возможности | PNG</span><span class="sxs-lookup"><span data-stu-id="2330c-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="2330c-107">[Корпоративная организация здравоохранения определяет состояние][WHODisabilities] "несоответствие" во время взаимодействия между функциями тела человека и возможностями среды, в которой они находятся.</span><span class="sxs-lookup"><span data-stu-id="2330c-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="2330c-108">Неограниченные возможности, такие как ограниченный мобильный доступ на телефоне, в том числе в другом физическом, подаудите, в других случаях.</span><span class="sxs-lookup"><span data-stu-id="2330c-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="2330c-109">Проектирование веб-сайтов и других технологий для включения создает впечатление для всех людей.</span><span class="sxs-lookup"><span data-stu-id="2330c-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="2330c-110">Инклюзивное проектирование и специальные возможности веб-сайта позволяют всем пользователям использовать веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="2330c-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="2330c-111">Ниже приведены некоторые рекомендации, примеры кода и другие ресурсы, которые помогут вам узнать больше о [проектировании][AccessibilityDesign], [создании][AccessibilityBuild]и [тестировании][AccessibilityTest] веб-сайтов со специальными возможностями в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2330c-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="2330c-112">Специальные возможности в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2330c-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="2330c-113">В Microsoft Edge мы предоставили современный [API автоматизации пользовательского интерфейса][WindowsWin32AutoEntryui] \ (UIA API \).</span><span class="sxs-lookup"><span data-stu-id="2330c-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="2330c-114">Изменение на модель UIA является значительным вкладом в специальные возможности браузера, и она размещает основу для более широких веб-интерфейсов пользователей, которые зависят от специальных возможностей в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2330c-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="2330c-115">Пользователи также выигрывают от Evergreen природы обработчика Chromium.</span><span class="sxs-lookup"><span data-stu-id="2330c-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="2330c-116">Система специальных возможностей в Microsoft Edge изначально поддерживает современные веб-стандарты, в том числе ARIA, HTML5 и CSS3.</span><span class="sxs-lookup"><span data-stu-id="2330c-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="2330c-117">Следующая схема упрощенного конвейера браузера следует за содержимым веб-страниц в доступном слое презентаций.</span><span class="sxs-lookup"><span data-stu-id="2330c-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Содержимое, преобразованное в модель обработчика, проецируется на визуальные и специальные представления, представленные как визуальная или доступная презентация.":::
   <span data-ttu-id="2330c-119">Рисунок 1.</span><span class="sxs-lookup"><span data-stu-id="2330c-119">Figure 1.</span></span>  <span data-ttu-id="2330c-120">Содержимое, преобразованное в модель обработчика, проецируется на визуальные и специальные представления, представленные как визуальная или доступная презентация.</span><span class="sxs-lookup"><span data-stu-id="2330c-120">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>
:::image-end:::

<!--![Figure 1.  Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation][ImageAccessibilityArchitecture]  -->  

<span data-ttu-id="2330c-121">Группа Microsoft EDGE работает вместе с поставщиками W3C и другими разработчиками браузера, чтобы убедиться в том, что новые возможности веб-платформы имеют достаточно встроенные специальные возможности.</span><span class="sxs-lookup"><span data-stu-id="2330c-121">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="2330c-122">Сведения о новых возможностях HTML5 accessibly, поддерживаемых Microsoft EDGE, можно найти в [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="2330c-122">For information on which new HTML5 features are accessibly supported by Microsoft Edge, visit [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="2330c-123">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="2330c-123">Resources</span></span>  

#### <span data-ttu-id="2330c-124">Блог о модели автоматизации пользовательского интерфейса Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="2330c-124">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="2330c-125">В [блоге по автоматизации пользовательского интерфейса Microsoft Windows][ArchiveBlogsWinuiautomation] рассматриваются темы, связанные с API автоматизации Windows.</span><span class="sxs-lookup"><span data-stu-id="2330c-125">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="2330c-126">Концепция специальных возможностей в Интернете (помощью ОРИЕНТИРОВ WAI)</span><span class="sxs-lookup"><span data-stu-id="2330c-126">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="2330c-127">Программа [поддержки специальных возможностей в Интернете (помощью ориентиров WAI)][W3CWaiHome] , в которой был представлен путь консорциума W3C, является значительным количеством усилий, которые помогут вам улучшить доступность веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2330c-127">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="2330c-128">На сайте доступны различные ресурсы для [начала работы со специальными возможностями в Интернете][W3CWaiGettingstartedOverview], [разработки для включения][W3CWaiFundamentals], [учебников и презентаций][W3CWaiTeachAdvocate]и т. д.</span><span class="sxs-lookup"><span data-stu-id="2330c-128">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  


<!-- image links -->  

<!--[ImageAccessibilityArchitecture]: ./media/accessibilityarchitecture.png "Figure 1: Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation"  -->  

<!-- links -->  

[AccessibilityBuild]: ./accessibility/build.md "Создание общедоступных веб-сайтов"  
[AccessibilityDesign]: ./accessibility/design.md "Создание веб-сайтов со специальными возможностями"  
[AccessibilityTest]: ./accessibility/test.md "Тестирование специальных возможностей"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Модель автоматизации пользовательского интерфейса"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Блог о модели автоматизации пользовательского интерфейса Microsoft Windows"  

[HTML5Accessibility]: https://html5accessibility.com "Специальные возможности HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Специальные возможности | PNG"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Общие сведения о специальных возможностях в Интернете | Инициатива веб-специальных возможностей (помощью ОРИЕНТИРОВ WAI) | PNG"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Приступая к работе: создание доступного веб-сайта | Инициатива веб-специальных возможностей (помощью ОРИЕНТИРОВ WAI) | PNG"  
[W3CWaiHome]: https://w3.org/wai "Инициатива веб-специальных возможностей (помощью ОРИЕНТИРОВ WAI) | PNG"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Обзор и обучите | Инициатива веб-специальных возможностей (помощью ОРИЕНТИРОВ WAI) | PNG"  

[WHODisabilities]: https://who.int/topics/disabilities "Ограниченные | РАБОТНИК"  


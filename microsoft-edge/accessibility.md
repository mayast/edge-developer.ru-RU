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
# Специальные возможности  

> "\ [T \] его влияние на световые возможности радикально изменилось в Интернете, так как в Интернете удаляются барьеры для общения и взаимодействия, которые многие люди сталкиваются с физическим миром." [(Специальные возможности | PNG][W3CAccessibility]  

[Корпоративная организация здравоохранения определяет состояние][WHODisabilities] "несоответствие" во время взаимодействия между функциями тела человека и возможностями среды, в которой они находятся.  Неограниченные возможности, такие как ограниченный мобильный доступ на телефоне, в том числе в другом физическом, подаудите, в других случаях.  

Проектирование веб-сайтов и других технологий для включения создает впечатление для всех людей.  Инклюзивное проектирование и специальные возможности веб-сайта позволяют всем пользователям использовать веб-сайт.  

Ниже приведены некоторые рекомендации, примеры кода и другие ресурсы, которые помогут вам узнать больше о [проектировании][AccessibilityDesign], [создании][AccessibilityBuild]и [тестировании][AccessibilityTest] веб-сайтов со специальными возможностями в Microsoft Edge.  

## Специальные возможности в Microsoft Edge  

В Microsoft Edge мы предоставили современный [API автоматизации пользовательского интерфейса][WindowsWin32AutoEntryui] \ (UIA API \).  Изменение на модель UIA является значительным вкладом в специальные возможности браузера, и она размещает основу для более широких веб-интерфейсов пользователей, которые зависят от специальных возможностей в Windows 10.  Пользователи также выигрывают от Evergreen природы обработчика Chromium.  

Система специальных возможностей в Microsoft Edge изначально поддерживает современные веб-стандарты, в том числе ARIA, HTML5 и CSS3.  Следующая схема упрощенного конвейера браузера следует за содержимым веб-страниц в доступном слое презентаций.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Содержимое, преобразованное в модель обработчика, проецируется на визуальные и специальные представления, представленные как визуальная или доступная презентация.":::
   Рисунок 1.  Содержимое, преобразованное в модель обработчика, проецируется на визуальные и специальные представления, представленные как визуальная или доступная презентация.
:::image-end:::

<!--![Figure 1.  Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation][ImageAccessibilityArchitecture]  -->  

Группа Microsoft EDGE работает вместе с поставщиками W3C и другими разработчиками браузера, чтобы убедиться в том, что новые возможности веб-платформы имеют достаточно встроенные специальные возможности.  

Сведения о новых возможностях HTML5 accessibly, поддерживаемых Microsoft EDGE, можно найти в [HTML5Accessibility][HTML5Accessibility].  

## Ресурсы  

#### Блог о модели автоматизации пользовательского интерфейса Microsoft Windows  

В [блоге по автоматизации пользовательского интерфейса Microsoft Windows][ArchiveBlogsWinuiautomation] рассматриваются темы, связанные с API автоматизации Windows.  

#### Концепция специальных возможностей в Интернете (помощью ОРИЕНТИРОВ WAI)  

Программа [поддержки специальных возможностей в Интернете (помощью ориентиров WAI)][W3CWaiHome] , в которой был представлен путь консорциума W3C, является значительным количеством усилий, которые помогут вам улучшить доступность веб-сайта.  На сайте доступны различные ресурсы для [начала работы со специальными возможностями в Интернете][W3CWaiGettingstartedOverview], [разработки для включения][W3CWaiFundamentals], [учебников и презентаций][W3CWaiTeachAdvocate]и т. д.  


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


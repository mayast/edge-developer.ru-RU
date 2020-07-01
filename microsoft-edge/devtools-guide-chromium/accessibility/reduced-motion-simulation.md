---
title: Имитация уменьшенного движения с помощью средств разработчика (CSS понижает движение)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: f1bf90de4ac1832fff07e9ac963c26f92adeea2c
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843986"
---
# Понижение моделирования движения  

Анимация в веб-продуктах может представлять собой проблему с читаемостью.  В операционных системах проблему можно решить, добавив параметр, позволяющий отключить анимацию, чтобы избежать путаницы и потенциальных проблем, связанных с работоспособностью, например инициирования захвата.  На веб-сайте вы можете использовать запрос на доступ к материалам CSS с [сокращенными][MDNPrefersReducedMotion] эффектами перемещения, чтобы определить, предпочитаете ли пользователи видеть анимацию.  В вашем продукте вы можете заключить код анимации в тест, чтобы избежать анимаций для затронутых пользователей.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

С помощью [Microsoft Edge DevTools][DevtoolsGuideChromiumMain]вы можете имитировать этот уменьшенный параметр перемещения, не изменяя операционную систему.  

1.  Открытие **меню команд**.  
    1.  Нажмите клавишу `Control` + `Shift` + `P` Windows или `Command` + `Shift` + `P` macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           **Меню команд**  
        :::image-end:::   
        
1.  Тип `reduced` , чтобы включить или отключить эмуляцию.  Выберите параметр и нажмите клавишу `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Включение и отключение параметра "предпочтительные уменьшенные перемещения" в меню команд" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Включение и отключение параметра " **предпочтительные уменьшенные перемещения** " в **меню команд**  
    :::image-end:::  
    
1.  Обновите текущую страницу, чтобы убедиться, что анимации выключены или отображаются.  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Рисунок 1: меню команд"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Рисунок 2: переключение уменьшенного движения из палитры команд"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft EDGE (Chromium) — Инструменты разработчика Microsoft | Документы Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "предпочитать — понижение уровня | MDN"  

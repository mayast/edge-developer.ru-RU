---
title: Эмуляция видения deficiencies в Microsoft Edge DevTools (жалюзи цвета)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843923"
---
# Эмуляция видения deficiencies

Чтобы лучше удовлетворить потребности пользователей с помощью [цветовой][ColorblindawarenessMain] платформы \ (ослабление цвета \), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] позволяет имитировать определенную концепцию deficiencies.  Средство **эмуляции deficiencies** имитирует следующие категории.  

| Некоторая концепция цвета | Сведения |  
|:--- |:--- |  
| Размытое видение | У пользователя возникли трудности с детальными сведениями. |   
| Protanopia | Пользователь не может воспринимать красный свет. |  
| Deuteranopia | Пользователь не может воспринимать зеленый свет. |  
| Tritanopia | Пользователь не может воспринимать синий свет. |  
| Achromatopsia | Пользователь не может воспринимать любой цвет, что сокращает цвет до оттенка серого. |  

## Переход к средствам отображения  

Чтобы смоделировать предметный ряд, применяемый для вашего веб-продукта, откройте [инструменты для подготовки к просмотру][RenderingTools].  

1.  Открытие средств рендеринга путем выбора `...` пункта меню на панели инструментов  
1.  Выбор `More tools`  
1.  Выбор `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств рендеринга" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Открытие **средств рендеринга**  
    :::image-end:::  

Меню **рендеринга** появится в ящике.  

1.  Прокрутите вниз до `Emulate vision deficiencies` пункта меню и щелкните раскрывающееся меню, чтобы отобразить параметры.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню симулятор deficiencies видения в ящике отрисовки" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Меню " **симулятор deficiencies видения** " в ящике **отрисовки**  
    :::image-end:::  
    
1.  Выберите один из вариантов.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню концепция имитации deficiencies" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Параметры меню " **концепция имитации deficiencies** "  
    :::image-end:::  
    
1.  В главном окне будет показана Эмуляция выбранного параметра, примененная к текущей странице.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Вывод на экран с помощью * * имитация размытого видения * *" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Отображение с помощью имитации **размытого видения**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Вывод на экран с помощью функции эмуляции * * Achromatopsia * *" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Отображение с помощью имитации **Achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Использование меню команд  

Вы также можете использовать **командное меню** для доступа к различным эмуляциям.  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       **Меню команд**  
    :::image-end:::  
    
1.  Введите текст `emulate` , который вы хотите имитировать, и нажмите `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные варианты моделирования, доступные в меню команд" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Различные варианты моделирования, доступные в **меню команд**  
    :::image-end:::  
    
> [!IMPORTANT]
> Средства **эмуляции deficiencies** помогают понять, как человек с каждым недостатком может видеть ваш продукт.  У каждого человека разный, поэтому концепция deficiencies по серьезности может варьироваться от человека к человеку.  Для более эффективного удовлетворения потребностей пользователей следует избегать цветовых сочетаний, которые могут быть причиной проблем.  Средства **имитации концепции deficiencies** не являются полным анализом специальных возможностей вашего продукта.  Вместо этого инструменты **эмуляции deficiencies** должны дать вам хороший первый шаг, чтобы избежать проблем.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация, в которой вы осведомлены о цвете"  
[AmfcbMain]: https://www.amfcb.org "Американская основа для цвета "вслепую" (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Инструменты для отрисовки Microsoft EDGE (Chromium)"  

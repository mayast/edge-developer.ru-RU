---
title: Эмуляция видения deficiencies в Microsoft Edge DevTools (жалюзи цвета)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758121"
---
# Эмуляция видения deficiencies

В любой стране мира около 8% от мужчин и 0,5% в женщин имеется [концепция цвета][ColorblindawarenessMain] , которая обычно называется "жалюзи цветов".  [Microsoft Edge DevTools][MicrosoftEdgeDevTools] позволяет эмулировать различные известные deficiencies и предоставлять предварительный просмотр продукта для проверки.  

| Цветовой недостатк | Сведения |  
|:--- |:--- |  
| Размытое видение |  |   
| Protanopia | Невозможность воспринимать красный индикатор. |  
| Deuteranopia | Невозможность воспринимать зеленый свет. |  
| Tritanopia | Невозможность воспринимать любой синий индикатор. |  
| Achromatopsia | Невозможность воспринимать любой цвет, кроме оттенков серого. |  

## Переход к средствам отображения  

Чтобы протестировать текущий веб-продукт в цвете deficiencies, откройте [инструменты рендеринга][RenderingTools].  

1.  Открытие средств рендеринга путем выбора `...` пункта меню на панели инструментов  
1.  Выбор `More tools`  
1.  Выбор `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств рендеринга" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Открытие **средств рендеринга**  
    :::image-end:::  

В нижней половине DevTools откроется меню **рендеринга** .  

1.  Прокрутите вниз до `Emulate Vision deficiencies` пункта меню и выберите один из вариантов.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню "эмулятор" deficiencies "инструменты для отрисовки"" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Меню " **эмулятор" deficiencies** "инструменты для **отрисовки** "  
    :::image-end:::  
    
1.  Выберите один из вариантов  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню "концепция имитации deficiencies"" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Параметры меню " **концепция имитации deficiencies** "  
    :::image-end:::  
    
1.  Текущая страница отображается в имитации того, как она может выглядеть для пользователя с выбранным недостатком.  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Документация по средствам разработчика Microsoft EDGE в эмуляции размытого видения" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Отображается с помощью эмуляции **размытого видения**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Документация по средствам разработчика Microsoft EDGE в эмуляторе концепции Achromatopsia" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Отображение с помощью эмуляции **концепции Achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Использование меню команд  

Кроме того, вы можете достичь разных эмуляций, не переходя между различными меню с помощью **меню команд**.  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       **Меню команд**  
    :::image-end:::  
    
1.  Введите текст `emulate` , который вы хотите имитировать, и нажмите `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные параметры эмуляции, доступные в меню команд" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Различные параметры эмуляции, доступные в **меню команд**  
    :::image-end:::  
    
> [!IMPORTANT]
> Средства эмуляции представляют собой приблизительные сведения о том, как человек с каждым недостатком может видеть ваш продукт.  У каждого человека разный, поэтому концепция deficiencies по серьезности может варьироваться от человека к человеку.  Для более эффективного удовлетворения потребностей пользователей следует избегать цветовых сочетаний, которые могут быть причиной проблем.  Средства эмуляции не полностью изменяют доступность вашего продукта, но у вас должен быть лучший первый шаг к устранению незначительных deficiencies.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация, в которой вы осведомлены о цвете"  
[AmfcbMain]: https://www.amfcb.org "Американская основа для цвета "вслепую" (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Инструменты для отрисовки Microsoft EDGE (Chromium)"  

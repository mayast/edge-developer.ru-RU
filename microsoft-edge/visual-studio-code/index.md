---
description: Microsoft EDGE (Chromium) и код Visual Studio
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик, веб-подсказка
ms.openlocfilehash: e178612d9db8ce3223bb5158c4557675d3314e15
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695887"
---
# Visual Studio Code  

[Код Visual Studio][VisualStudioCodeDocs] — это упрощенный, но мощный редактор исходного кода, который работает на вашем компьютере и доступен для Windows, MacOS и Linux.  Она включает встроенную поддержку JavaScript, TypeScript и Node. js, поэтому она является прекрасным средством для веб-разработчиков прямо из этого поля.  Если вы еще не используете его, скачайте [код Visual Studio][VisualstudioCode].  

## Расширения  

<!--Todo: We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Чтобы получить любое из расширений, выбранных ниже, перейдите к разделу расширения \ ( `Ctrl` + `Shift` + `X` в Windows или `Command` + `Shift` + `X` на macOS \) в коде vs.  

Найдите нужное расширение рынка и нажмите кнопку **установить**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Установка отладчика для расширения кода Microsoft Edge VS":::
   Установка отладчика для расширения кода Microsoft Edge VS  
:::image-end:::  

:::row:::
   :::column span="1":::
      ### Отладчик для Microsoft Edge  

      С помощью [отладчика для расширения кода Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] VS выполните построчное отладку кода JavaScript и просмотрите `console.log()` Операторы прямо из [кода Visual Studio][VisualstudioCode]!  
      
      С помощью средства отладки вы можете запустить и присоединиться к обоим Microsoft Edge \ (EdgeHTML \) и Microsoft Edge \ (Chromium \).  Пошаговое руководство по отладке Microsoft Edge из кода VS и образцов `launch.json` конфигураций можно найти в разделе [отладчик для расширения кода Microsoft Edge VS][VscodeDebuggerEdge].  Выберите изображение на рисунке, чтобы увидеть расширение в действии.  

      :::image type="content" source="./media/debugger-for-edge.png" alt-text="Отладчик для расширения кода EDGE в действии" lightbox="./media/debugger-for-edge.gif":::  
   :::column-end:::
   :::column span="1":::
      ### Элементы Microsoft Edge  
      
      С помощью [элементов для расширения кода Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS используйте инструмент "элементы" браузера Microsoft EDGE в коде Visual Studio.  Как при запуске, так и при присоединении средство "элементы" подключается к экземпляру Microsoft EDGE, отображает структуру HTML среды выполнения и позволяет изменить макет или проблемы со стилизацией.  
      
      Дополнительные сведения можно найти в разделе [элементы расширения кода Microsoft EDGE и][VscodeElementsEdge].  Выберите изображение на рисунке, чтобы увидеть расширение в действии.  
      
      :::image type="content" source="./media/elements-for-edge.png" alt-text="Элементы для расширения кода EDGE в действии" lightbox="./media/elements-for-edge.gif":::  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      ### webhint
      
      Используйте веб- [подсказку][WebhintMain], настраиваемый инструмент linting, чтобы улучшить доступность, производительность, совместимость с различными браузерами, совместимость с PWA и безопасность сайта.  Она проверяет ваш код на предмет рекомендаций и распространенных ошибок. Проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation][OpenjsFoundation].  Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.  <!--Select the following image to see the extension in action.  -->  
      
      :::image type="content" source="./media/webhint-extension.png" alt-text="Снимок экрана: расширение кода и ссылки на него" lightbox="./media/webhint-extension.png":::  
      
      Выявление и устранение проблем в HTML, CSS, JavaScript, TypeScript и т. д. Добавьте расширение веб- [подсказки для кода VS][VisualstudioMarketplaceWebhint].  Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели " **проблемы** ".  
      
      Дополнительные сведения можно найти [в разделе Использование подсказки в коде Visual Studio][VscodeWebhint].  
   :::column-end:::
   :::column span="1":::
      <!--Empty to retain grid  -->  
   :::column-end:::
:::row-end:::

<!-- image links -->  

<!--links -->  

[VscodeDebuggerEdge]: ./debugger-for-edge.md "Отладчик для расширения кода Microsoft Edge VS | Документы Microsoft"  
[VscodeElementsEdge]: ./elements-for-edge.md "Элементы для расширения Microsoft EDGE и кода Документы Microsoft"  
[VscodeWebhint]: ./webhint.md "Расширение ссылки и кода Документы Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладчик для Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Элементы для Microsoft EDGE (Chromium) | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "Подсказка | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "Подсказка"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

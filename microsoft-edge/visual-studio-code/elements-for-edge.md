---
description: Использование элементов для Microsoft EDGE (Chromium) из кода VS
title: Элементы для Microsoft EDGE (Chromium) из кода VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, элементы
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694864"
---
# Элементы расширений Microsoft EDGE и кода  

С помощью [элементов для расширения кода Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS используйте инструмент "элементы" браузера Microsoft EDGE в [коде Visual Studio][VisualstudioCode].  Как при запуске, так и при присоединении средство "элементы" подключается к экземпляру Microsoft EDGE, отображает структуру HTML среды выполнения и позволяет изменить макет или проблемы со стилизацией.  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Элементы для расширения кода EDGE на работе":::
   Элементы для расширения кода EDGE на работе  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## Запуск Microsoft Edge из расширения Elements  

Перейдите к элементам на **панели действий**.  Рядом с надписью **элементы для Microsoft Edge: targets** — знак "плюс", который открывает браузер для вашего приложения.  Если вы выбрали параметр **about: Blank** , вы должны перейти в браузере, чтобы он отображался на панели элементов в коде vs.  

## Запуск Microsoft Edge из представления отладки  

Если вы привыкли использовать представление отладку в коде Visual Studio, вы можете получить доступ к элементам из этого инструмента.  Перейдите в представление Отладка \ ( `Ctrl` + `Shift` + `D` в Windows или `Command` + `Shift` + `D` на macOS \).  

Если у вас нет каких бы то ни было конфигураций в коде VS, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** . Выберите **ребро** в раскрывающемся списке. Вы увидите `launch.json` файл со следующей конфигурацией.  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```  

После того как вы загрузили правильную конфигурацию, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** . С помощью инструмента "элементы", который знаком вам, из браузера Microsoft Edge запускается в коде VS, что позволяет получать доступ к ролика браузера и просматривать компоненты страницы.  

## Присоединение к Microsoft Edge  

Чтобы прикрепить код VS к экземпляру Microsoft Edge \ (Chromium \), необходимо запустить браузер, выполнив следующую команду на экране терминала.  

`start msedge --remote-debugging-port=9222`  

После запуска приложения добавьте указанную ниже конфигурацию в файл **Launch. JSON** .  

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```  

Выберите команду **присоединиться к Microsoft EDGE и откройте средство элементы** из раскрывающегося меню отладчик.  Затем либо нажмите `F5` на Windows, либо macOS либо нажмите зеленую кнопку **воспроизведения** .  Код VS запускает инструмент элементы, позволяя получить доступ к экранной роли браузера, проверить модель DOM и стиль компонентов на странице.  

## Связь с элементами для группы расширения кода Microsoft Edge VS  

Отправьте отзыв, выполнив [архивацию][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] в расширении.  

Если вы хотите лучше сделать элементы для расширения кода Microsoft EDGE и более, ваши публикации будут рады!  Найдите все, что нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] на расширение.  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
[ImagePngElementsEdge]:./Media/Elements-for-Edge.png "элементы для расширения кода пограничного или более ранней программы в действии"  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Элементы для расширения Microsoft EDGE и кода Документы Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-Devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Новая ошибка — Microsoft/vscode-Edge-Devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Элементы для Microsoft EDGE (Chromium) | Visual Studio Marketplace"  

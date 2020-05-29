---
description: Отладка Microsoft EDGE (Chromium) и Microsoft EDGE (EdgeHTML) из кода VS
title: Отладка Microsoft EDGE (Chromium) из кода VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572804"
---
# Отладчик для расширения кода Microsoft Edge VS

С помощью [отладчика для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS вы можете выполнять отладку клиентского кода JavaScript по строкам и просматривать `console.log()` инструкции прямо из [кода Visual Studio](https://code.visualstudio.com/)!

![GIF-файл с отладчиком для расширения кода пограничного и на рабочем процессе](./media/debugger-for-edge.gif)

## Запуск Microsoft Edge

Перейдите в представление Отладка ( `Ctrl`  +  `Shift`  +  `D` в Windows или `Command`  +  `Shift`  +  `D` на компьютере Mac) на **панели действий**. Если у вас нет каких-либо конфигураций в коде VS, нажмите клавишу `F5` Windows или Mac или нажмите зеленую кнопку **воспроизведения** . В раскрывающемся списке выберите пункт "Edge". Теперь появится файл **Launch. JSON** со следующими конфигурацией.

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```

Если вы нажмете `F5` кнопку « **воспроизвести** зеленый» в Windows или Mac или снова нажмите зеленую кнопку воспроизведения, код VS будет запускать Microsoft EDGE (EdgeHTML), и вы сможете выполнять отладку любого веб-проекта, который вы используете на порте **8080** прямо из кода VS!

### Microsoft Edge (на основе Chromium)

Если вы хотите запустить Microsoft EDGE (Chromium), в следующей версии Microsoft EDGE вместо Microsoft EDGE (EdgeHTML) просто добавьте `version` атрибут для существующей конфигурации с версией Microsoft EDGE (Chromium), которую вы хотите запустить ( `dev` `beta` или `canary` ). Указанные ниже конфигурации запустят версию Канарские Microsoft EDGE (Chromium):

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```

## Присоединение к Microsoft Edge

Вы также можете прикрепить код VS к Microsoft EDGE (Chromium). На своем терминале выполните следующую команду:

`start msedge --remote-debugging-port=9222`

Добавьте в файл **Launch. JSON** конфигурацию ниже.

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

Если теперь вы запустите такую конфигурацию, код VS будет подсоединен к Microsoft EDGE (Chromium), и вы сможете начать отладку!

## Отзыв

Отправьте нам отзыв, выполнив [архивацию](https://github.com/Microsoft/vscode-edge-debug2/issues/new) в [репозитории GitHub](https://github.com/Microsoft/vscode-edge-debug2)для этого расширения. Добавьте файл журнала адаптера отладки, который создается для каждого запуска в каталоге% TEMP% с именем `vscode-edge-debug2.txt` . Вы можете перетащить этот файл в комментарий вопроса, чтобы отправить его в GitHub.

Если вы хотите помочь нам улучшить это расширение, мы будем рады вашим публикациям! Вы можете найти все, что вам нужно, чтобы приступить к работе в [нашем репозитории GitHub](https://github.com/Microsoft/vscode-edge-debug2).
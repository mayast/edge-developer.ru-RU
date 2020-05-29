---
description: Использование элементов для Microsoft EDGE (Chromium) из кода VS
title: Элементы для Microsoft EDGE (Chromium) из кода VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, элементы
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572808"
---
# Элементы расширений Microsoft EDGE и кода

Добавляя [элементы для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) и вы можете использовать средство браузера Elements в [коде Visual Studio](https://code.visualstudio.com/). При запуске или присоединении средство "элементы" подключится к экземпляру Microsoft EDGE, отобразит HTML-структуру среды выполнения и позволит вам изменить макет или устранить проблемы с стилизацией.

![GIF-файл с элементами для расширения кода пограничного и на рабочем процессе](./media/elements-for-edge.gif)

## Запуск Microsoft Edge из расширения Elements 

Перейдите к элементам на **панели действий**. Рядом с надписью "элементы для Microsoft Edge: targets" есть знак "плюс", который будет открывать браузер для вашего приложения. Если вы выбрали параметр *about: Blank* , вам придется перейти к веб-приложению в браузере, чтобы оно отображалось на панели элементы в коде vs.

## Запуск Microsoft Edge из представления отладки

Если вы привыкли использовать представление отладку в коде Visual Studio, вы можете получить доступ к элементам этого средства. Перейдите в представление Отладка ( `Ctrl`  +  `Shift`  +  `D` в Windows или `Command`  +  `Shift`  +  `D` на компьютере Mac). 

Если у вас нет каких-либо конфигураций в коде VS, нажмите клавишу `F5` Windows или Mac или нажмите зеленую кнопку **воспроизведения** . В раскрывающемся списке выберите пункт "Edge". Теперь появится файл **Launch. JSON** со следующими конфигурацией.

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

После того как вы загрузили правильную конфигурацию, нажмите клавишу `F5` Windows или Mac или нажмите зеленую кнопку **воспроизведения** . Инструмент элементы, знакомый с обозревателем Microsoft EDGE, теперь будет запущен в рамках кода VS, что позволит вам получить доступ к ролика браузера и проверить компоненты страницы.

## Присоединение к Microsoft Edge
Если вы хотите прикрепить код VS к экземпляру Microsoft EDGE (Chromium), необходимо запустить браузер, выполнив следующую команду из teminal:

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

Выберите "присоединиться к Microsoft Edge" и откройте инструмент "элементы" в раскрывающемся меню "отладчик". После этого нажмите `F5` на Windows или Mac или нажмите зеленую кнопку **воспроизведения** . Код VS запустит инструмент элементы, что позволит вам получить доступ к экранной роли браузера, проверить модель DOM и стиль компонентов на странице.

## Отзыв
Отправьте нам отзыв, выполнив [архивацию](https://github.com/microsoft/vscode-edge-devtools/issues/new) в [репозитории GitHub](https://github.com/microsoft/vscode-edge-devtools)для этого расширения. 

Если вы хотите помочь нам улучшить это расширение, мы будем рады вашим публикациям! Вы можете найти все, что вам нужно, чтобы приступить к работе в [нашем репозитории GitHub](https://github.com/microsoft/vscode-edge-devtools).
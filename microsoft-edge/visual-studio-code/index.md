---
description: Microsoft EDGE (Chromium) и код Visual Studio
title: Visual Studio Code
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик, веб-подсказка
ms.openlocfilehash: 94148864edbd43adbe2dc9f3d0c2fa0c1f7f0b43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572807"
---
# Visual Studio Code

[Код Visual Studio](https://code.visualstudio.com/Docs) — это упрощенный, но мощный редактор исходного кода, который работает на вашем компьютере и доступен для Windows, MacOS и Linux. Она поставляется с встроенной поддержкой JavaScript, TypeScript и Node. js, так что это отличный инструмент для веб-разработчиков прямо из этого поля. Заголовку на [эту страницу](https://code.visualstudio.com/) , чтобы загрузить код Visual Studio, если он еще не используется.

## Расширения

<!-- We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page. I think it's a web page. I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->

Чтобы получить какое-либо из расширений, выделенных ниже, перейдите в раздел расширения ( `Ctrl`  +  `Shift`  +  `X` в Windows или `Command`  +  `Shift`  +  `X` Mac) в код vs.

Найдите нужное расширение рынка и нажмите кнопку **установить**.

![Установка отладчика для расширения кода Microsoft Edge VS](./media/vscode-debugger-install.png)

## Отладчик для Microsoft Edge

Проведите отладку кода JavaScript на строке по строкам и выведите `console.log()` Операторы прямо в [коде Visual Studio](https://code.visualstudio.com/) с помощью [отладчика для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs.

Используйте [отладчик для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS, чтобы запустить и присоединиться к Microsoft EDGE (EdgeHTML) и Microsoft EDGE (Chromium). Ознакомьтесь со [this page](./debugger-for-edge.md) статьей, пошаговыми инструкциями по отладке Microsoft Edge из кода VS и примерами настроек **Launch. JSON** .

![GIF-файл отладчика для расширения кода пограничного или более ранней версии в действии!](./media/debugger-for-edge.gif)

## Элементы Microsoft Edge

Добавляя [элементы для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) и вы можете использовать средство браузера Elements в коде Visual Studio. При запуске или присоединении средство "элементы" подключится к экземпляру Microsoft EDGE, отобразит HTML-структуру среды выполнения и позволит вам изменить макет или устранить проблемы с стилизацией.

Дополнительные сведения можно найти на [этой странице](./elements-for-edge.md).

![GIF-файл для расширения кода пограничного элемента в действии!](./media/elements-for-edge.gif)

## Подсказка

Используйте веб- [подсказку](https://webhint.io), настраиваемый инструмент linting, чтобы улучшить доступность, производительность, совместимость с различными браузерами, совместимость с PWA и безопасность сайта. Она проверяет ваш код на предмет рекомендаций и распространенных ошибок. Этот проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation](https://openjsf.org/). Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.

![Снимок экрана: расширение кода и ссылки на него](./media/webhint-extension.png)

Выявление и устранение проблем в HTML, CSS, JavaScript, TypeScript и т. д. Добавьте расширение веб- [подсказки для кода VS](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint). Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели "проблемы".

Дополнительные сведения можно найти [в разделе Использование подсказки в коде Visual Studio](./webhint.md).

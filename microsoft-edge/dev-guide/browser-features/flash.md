---
description: Предоставьте удобный интерфейс на сайтах, для которых требуется Adobe Flash.
title: Flash — руководство для разработки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработка веб-приложений, мигание
ms.openlocfilehash: 33ee1c782fc969b2251ed075a59d8fa61bf61831
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942032"
---
# Flash  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Adobe Flash была интегрирована в веб-приложения для десятков, влияющая разнообразное содержимое и анимации в браузерах, так как перед HTML5 был введен формат HTML5.  В современных браузерах просроченные в современных браузерах прошу трансформации, а также веб-сайты, которые проводятся корпорацией Майкрософт, Adobe, Google, Apple, Mozilla и многие другие, поэтому возможности будут работать на сайтах, чтобы заранее использовать устройство flash и улучшенные производительность и безопасность.  Работать с партнерами других поставщиков браузера и adobe мы настоятельно рекомендуем разработчикам перенести их в стандарты HTML5, в [том](https://developer.microsoft.com/microsoft-edge/platform/status/encryptedmediaextensions)числе зашифрованные расширения мультимедиа, расширения по исходных медиаданных, [Canvas,](https://developer.microsoft.com/microsoft-edge/platform/status/canvas)Web Audio и [Media Source Extensions](https://developer.microsoft.com/microsoft-edge/platform/status/mediasourceextensions) [Real-Time Communication.](https://developer.microsoft.com/microsoft-edge/platform/status/webrtcobjectrtcapi) [Web Audio](https://developer.microsoft.com/microsoft-edge/platform/status/webaudioapi)  

В выпуске Microsoft Edge для Windows 10 в октябре 2018 г. мы продолжаем улучшать продолжение поддержки Flash Deprecation в рамках [конца поддержки Adobe после выпуска Adobe](https://theblog.adobe.com/adobe-flash-update) после выпуска 2021 года. [covered](https://blogs.windows.com/msedgedev/2017/07/25)  В октябре 2018 г. пользователям будет необходимо явно разрешать установку Флэш-памяти на сайте в течение жизненного цикла вкладки.  Функция "Постоянное доступен" больше не доступна, и пользователь не сможет управлять разрешениями на флэш-вкладку, доступную вкладок.  

Во время перехода на стандарты HTML5 можно сделать несколькими простыми принципами, которые посещают вашвеб сайт в браузере Microsoft Edge в Windows 10 Creators Update.  

Если на странице используется флажок, но пользователь не включил ее, Microsoft Edge обычно показывает значок круговой диаграммы в адресной строке, как показано в [этом блоге.](https://blogs.windows.com/msedgedev/2016/12/14)  Если элемент управления "Мгновенно" добавляется после загрузки страницы, значок кругового сектора может не отображаться.  В этом случае лучше проверить состояние присутствия мгновенного и предоставить ссылку, как описано ниже.  

Чтобы всем пользователям было хорошо обычная удобная реальная удобная реальная удобная процедура, проверьте сведения о присутствии для флэш-памяти с использованием стандартных механизмов.  Если Microsoft Edge недоступен для Flash, предоставьте пользователю ссылку для скачивания [Flash](http://get.adobe.com/flashplayer) и [скачайте флэш-загрузку](http://www.adobe.com/legal/permissions/icons-web-logos.html#flashplayer) для пользователя.  Когда пользователь щелкает ссылку, Microsoft Edge \(а также в других браузерах\) отобразятся запросы включить службу Flash Player для сайта.  Эта ссылка указывается в основном домене, для которого вы хотите включить эту функцию.  Она не будет работать, если вы перенаправите пользователей на страницы других доменов.  [Ниже приведен более демонстрация](https://microsoftedge.github.io/MicrosoftEdge-Documentation/flashclicktorun) предложенного интерфейса и соответствующего [кода.](https://github.com/MicrosoftEdge/MicrosoftEdge-Documentation/tree/master/docs/flashclicktorun)  

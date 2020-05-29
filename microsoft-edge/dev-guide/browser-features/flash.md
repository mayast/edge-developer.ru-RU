---
description: Обеспечьте бесперебойную работу пользователей на сайтах, требующих Adobe Flash.
title: Руководство по разработке — Flash
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, Flash
ms.openlocfilehash: b3e2efe142142b7cdf233acfc4e915cd320b556d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570901"
---
# Вспышка

Adobe Flash является неотъемлемой частью Интернета в десятках лет, позволяя использовать форматированное содержимое и анимацию в браузерах, начиная с того момента, когда была представлена функция HTML5. В современных браузерах веб-стандарты, добавленные корпорацией Майкрософт, Adobe, Google, Apple, Mozilla и многим другим пользователям, теперь позволяют сайтам превысить эти возможности без вспышки и улучшить производительность и безопасность. Совместная работа с другими поставщиками браузеров и приложениями Adobe настоятельно рекомендует разработчикам переходить к стандартам HTML5, в том числе к [зашифрованным расширениям мультимедиа](https://developer.microsoft.com/microsoft-edge/platform/status/encryptedmediaextensions), [расширениям источника мультимедиа](https://developer.microsoft.com/microsoft-edge/platform/status/mediasourceextensions), [холсту](https://developer.microsoft.com/microsoft-edge/platform/status/canvas), [веб-звуку](https://developer.microsoft.com/microsoft-edge/platform/status/webaudioapi)и [обмену данными в режиме реального времени](https://developer.microsoft.com/microsoft-edge/platform/status/webrtcobjectrtcapi).

С помощью выпуска Oct 2018 для Windows 10 Microsoft Edge продолжает усилия по отключению флэш-памяти, [которые мы](https://blogs.windows.com/msedgedev/2017/07/25/flash-on-windows-timeline/#9mCF959eQEK0poo5.97) выработали в рамках [объявления компании Adobe](https://theblog.adobe.com/adobe-flash-update/) о прекращении поддержки после 2021. В выпуске Oct 2018 вам потребуется явным образом разрешить запуск Flash на сайте в течение всего срока действия вкладки. Параметр постоянная возможность всегда будет недоступен, и пользователь не сможет управлять разрешением на флэш-память, занимающего сеансы табуляции.

При переходе к стандартам HTML5 есть несколько простых вещей, которые можно использовать для обеспечения положительного опыта ваших пользователей на веб-сайте с помощью Microsoft EDGE в обновлении Windows 10 Creators. 

Если на странице используется Flash, но пользователь не включил его, то Microsoft Edge обычно отображает в адресной строке значок головоломки, как показано в [этом блоге](https://blogs.windows.com/msedgedev/2016/12/14/edge-flash-click-run/#41svu6EMwKIAaigx.97). Если вы динамически добавляете элемент управления Flash после загрузки страницы, этот значок головоломки может не отображаться – в этом случае лучше всего протестировать наличие Flash и предоставить ссылку, как описано ниже.

Чтобы убедиться в том, что все пользователи имеют хорошее взаимодействие, продолжайте тестирование на наличие Flash с помощью стандартных механизмов. Если в Microsoft Edge есть сообщение о том, что флэш-память недоступна, выводится [ссылка Загрузить Flash](http://get.adobe.com/flashplayer) и [изображение загрузки флэш-памяти](http://www.adobe.com/legal/permissions/icons-web-logos.html#flashplayer) для пользователя. Когда пользователь щелкает ссылку, Microsoft EDGE (так же как и другие браузеры) предоставляет вам необходимые запросы на включение Flash Player для сайта. Ссылка должна появиться на основном домене, в котором вы хотите включить поддержку Flash. Если вы перенаправляли пользователей на страницы других доменов, это не повлияет на работу.  [Ниже приведена демонстрация](https://microsoftedge.github.io/MicrosoftEdge-Documentation/flashclicktorun/) предлагаемого опыта и соответствующего [примера кода](https://github.com/MicrosoftEdge/MicrosoftEdge-Documentation/tree/master/docs/flashclicktorun).

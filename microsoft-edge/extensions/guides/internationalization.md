---
description: Сделайте расширение доступным для разных языков и протестируйте строки языка с помощью руководства по интернационализации.
title: Расширения-Международная связь
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: d1f553d0e3e39192e68665fe6720daa811777c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571534"
---
# Интернационализация  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Для того чтобы расширение было доступно разным людям, важно учитывать особенности работы в других странах. С помощью расширений Microsoft EDGE можно добавлять в расширения различные языковые строки, чтобы их можно было легко изменить.

Дополнительные сведения о internationalizing вашего расширения можно найти в [руководстве по локализации](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)MDN.


## Языки тестирования

Чтобы протестировать языковые строки, сначала необходимо установить для языка интерфейса Windows язык, на котором вы хотите протестировать.

Чтобы изменить язык интерфейса Windows, выполните указанные ниже действия.

1. Откройте приложение параметры.

   ![приложение параметров](./../media/loc-settings.png)
2. Выберите "язык & времени".
3. Выберите пункт "регион & язык".
4. Выберите "+ добавить язык", чтобы добавить язык в список возможных языков.
5. Выберите язык из списка "языки", который вы хотите протестировать.
6. Нажмите кнопку "по умолчанию" (возможно, потребуется перезагрузить компьютер).
7. Откройте Microsoft EDGE и убедитесь в том, что строки, определенные для языкового стандарта, отображаются должным образом.

С помощью свойства [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) вы можете убедиться, что язык, который Microsoft Edge определяет, правильно установлен на языке интерфейса Windows.

Нажмите кнопку в CodePen ниже, чтобы увидеть язык интерфейса браузера.

<iframe height='300' scrolling='no' title='Получить языковой стандарт' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь со <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> статьей получение региональных параметров в </a> MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) на <a href='http://codepen.io'> CodePen </a> .
</iframe>

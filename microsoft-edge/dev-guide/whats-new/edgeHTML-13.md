---
description: На этой странице представлен обзор новых возможностей Microsoft EdgeHTML 13.
title: Новые функции и API в Microsoft EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 033b8dacb107492624f3b8c7775a47285c9893dd
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941912"
---
# Новые возможности В EdgeHTML 13  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Ниже перечислены изменения, пытаемые вместе с Браузером Microsoft Edge HTML 13, технологичным способом, который модуль Microsoft Edge в первом [обновлении](https://blogs.windows.com/windowsexperience/2015/11/12) Windows 10 \(11.11.2015, сборка 10586\).  Обзор изменений общего браузера Microsoft Edge см. в статье ["Знакомство с Microsoft EdgeHTML 13, нашем первоначальномплатформе microsoft Edge.](https://blogs.windows.com/msedgedev/2015/11/16)  

Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md)  

## Возможности  

### CSS  

EdgeHTML 13 поддерживает новые возможности CSS, включая следующие:  

*   [Классы CSS mutability Pseudo-Class-class-class-classes](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [CSS Range Pseudo-classes](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   При настройке и [избавлении ключевых слов](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) CSS [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue)  

### Зашифрованные расширения мультимедиа  

Теперь Microsoft Edge теперь поддерживает новые API непрефиксированных зашифрованных оболочки [мультимедиа.](https://w3.org/TR/encrypted-media)  Зашифрованные расширения мультимедиа \(EME\) расширяют элементы видео и звуковых данных, чтобы включить защиту содержимого без использования подключаемого модуля.  Дополнительные сведения о EME: [зашифрованные расширения мультимедиа.](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API)  

### Графика  

EdgeHTML 13 содержит следующие обновления графических элементов:  

*   [Холлст](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [Модели ломаны](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> элемент](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [Внешний контент SVG](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### JavaScript  

EdgeHTML 13 содержит основные улучшения и новые возможности поддержки [в Какра,](https://blogs.windows.com/msedgedev/2015/09/30)включая переключатель JavaScript, работает на диске, включая следующие:  

#### Новые возможности  

Включено по умолчанию  

*   [asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) по умолчанию (запись[блога),](https://blogs.windows.com/msedgedev/2015/11/10) [демонстрация \.](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)  
*   [Классы](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)  

#### Экспертные функции JavaScript  

Доступно с `about:flags`  

*   [Функции асинхронизации](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)  
*   [Оператор экспоненциального оператора](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)  
*   [Разработка](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)  

### Ввод пользователя  

В Microsoft EdgeHTML 13 появилась возможность ввода пользователей:  

*   [<meter> элемент](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [oninvalid event обработчик событий для документа и окна](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### Блокировка указате  

Теперь Microsoft Edge теперь поддерживает API блокировки указателя \(ранее называемая блокировка мыши\) для доступа к неперемещаемому перемещению, блокировке целевого элемента, уберение пределов продолжения перемещения в одном направлении и удаление курсора из вида.  

## Новые API в Microsoft EdgeHTML 13  

Ниже приведен полный список новых aPI в Microsoft EdgeHTML 13.  Они указаны в `[interface name].[api name]` формате.  

<iframe height='584' scrolling='no' title='Новые API в Microsoft EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'>См. раздел <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> "Новые API" в Microsoft EdgeHTML 13 </a> с помощью приложений Microsoft Edge <a href='http://codepen.io/MicrosoftEdgeDocumentation'> </a> (@MicrosoftEdgeDocumentation) на <a href='http://codepen.io'> коде </a> кода.</iframe>  

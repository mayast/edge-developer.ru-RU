---
description: На этой странице представлены общие сведения о новых возможностях EdgeHTML 13.
title: Новые возможности в EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: 8fb9d6bd78af5d595e217fa2bf210632f4c1a61f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570883"
---
# Новые возможности в EdgeHTML 13
Ниже приведены изменения, которые поставляются вместе с EdgeHTML 13-й системой, которая включает браузер Microsoft EDGE в [первое крупное обновление](https://blogs.windows.com/windowsexperience/2015/11/12/first-major-update-for-windows-10-available-today/) для Windows 10 (11/2015, сборка 10586). Общие сведения об изменениях, внесенных в общий браузер Microsoft EDGE, приведены в [статье Знакомство с EdgeHTML 13 и первой версией платформы Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16/introducing-edgehtml-13-our-first-platform-update-for-microsoft-edge/).

Ниже приведен список постоянных [https://aka.ms/devguide_edgehtml_13](https://aka.ms/devguide_edgehtml_13) изменений.

## Функции

### CSS
"" EdgeHTML 13 поддерживает новые функции CSS, в том числе:
* [Псевдо-классы для постоянство стилей CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses/)
* [Псевдо-классы с диапазоном CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses/)
* [Начальные](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue/) и [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue/) Неотмененные ключевые слова CSS

### Расширения зашифрованных файлов мультимедиа
Microsoft EDGE теперь поддерживает новые API-интерфейсы с непрефиксными [зашифрованными расширениями мультимедиа](https://w3.org/TR/encrypted-media/) . Расширения для зашифрованных мультимедийных файлов (ОБНОВЛЕННОЙ) расширяют элементы видео и звука, чтобы включить защищенное содержимое с помощью управления цифровыми правами (DRM), не используя подключаемые модули. Подробнее о ОБНОВЛЕННОЙ: [зашифрованные расширения для мультимедиа](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/encrypted-media-extensions).

### Графика

В EdgeHTML 13 появились следующие обновленные графические элементы:
* [Эллипс для холста](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse/)
* [Режимы наложения «холсты»](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d/)
* [`<picture>` элемент](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement/)
* [Внешнее содержимое SVG](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent/)

### JavaScript
EdgeHTML 13 содержит [существенные улучшения и поддержку новых функций в Chakra](https://blogs.windows.com/msedgedev/2015/09/30/asynchronous-code-gets-easier-with-es2016-async-function-support-in-chakra-and-microsoft-edge/), а также в Microsoft EDGE, включенный в ядро JavaScript, в том числе:

#### Новые функции (по умолчанию)

* [ASM. js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) включен по умолчанию ([запись блога](https://blogs.windows.com/msedgedev/2015/11/10/supercharging-javascript-performance-with-asm-js/), [демонстрация](https://dev.windows.com/microsoft-edge/testdrive/demos/chess/))
* [Классы](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) (ES2015)

#### Экспериментальные функции JavaScript (включены с *флагами about: flags*)

* [Асинхронные функции](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) (ES2016)
* [Оператор возведения](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) в степень (ES2016)
* [Разструктуризация](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) (ES2015)

### Ввод данных пользователем
Ниже перечислены функции, представленные в EdgeHTML 13 улучшения ввода данных пользователем.
* [`<meter>` элемент](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement/)
* [`oninvalid` обработчик событий для документа и окна элемента](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler/)

### Блокировка указателя
Microsoft EDGE теперь поддерживает интерфейс API блокировки указателей (ранее называемый блокировкой мыши) для доступа к перемещению мыши, заблокирующий цель событий мыши для одного элемента, устраняя ограничения того, насколько далеко движение мыши может находиться в одном направлении, и удаляет курсор из представления. 


## Новые API-интерфейсы в EdgeHTML 13 "" "

Ниже приведен полный список новых API-интерфейсов в EdgeHTML 13. Они указаны в формате **[имя интерфейса]. [ Имя API]**.
<iframe height='584' scrolling='no' title='Новые API-интерфейсы в EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь с <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> новыми API-интерфейсами в EdgeHTML 13 на </a> Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) на <a href='http://codepen.io'> CodePen </a> .</iframe>""''""''""

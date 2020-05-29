---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Это руководство содержит общие сведения о функциях и стандартах разработчика, включенных в Microsoft Edge.
title: Руководство для разработчиков
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: 36c5e6530ff584a97e4b42910757495362a1960d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570916"
---
# Новые возможности EdgeHTML 16

Ниже приведен список новых и обновленных функций, выпущенных на веб-платформах [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17/edgehtml-16-fall-creators-update/) в рамках [обновления Windows 10 для дизайнеров](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update/) (10/2017, сборка 16299). Изменения в конкретных сборках Insider Preview для Windows можно найти в [журнале изменений Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) и [о новых](../whats-new.md)возможностях EdgeHTML.

Ниже приведен список постоянных [https://aka.ms/devguide_edgehtml_16](https://aka.ms/devguide_edgehtml_16) изменений.

## Новые и обновленные функции

### Макет сетки CSS

Microsoft EDGE теперь поддерживает непрефиксную реализацию [макета сетки CSS](https://www.w3.org/TR/css-grid-1/). [Макет Grid](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) определяет двухмерную систему макета, основанную на сетке, которая обеспечивает более плавную работу с макетом, чем возможно при размещении с помощью одномерного или письменного представления. В примере ниже используется макет Grid CSS для создания структуры для базовой веб-страницы.


<iframe height='303' scrolling='no' title='Макет сетки CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Посмотрите <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> макет сетки стилей </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) в <a href='https://codepen.io'> CodePen </a> .
</iframe>


### CSS `object-fit` и `object-position`

В EdgeHTML 16 представлена поддержка свойств CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) и [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Эти свойства управляют положением и размером заменяемого содержимого в окне содержимого.  

### Средства разработчика

В этом выпуске мы приступили к тому, чтобы повысить надежность и производительность, а также добавить набор новых функций, которые можно использовать сегодня в сборках для программы [предварительной оценки Windows](https://insider.windows.com/) (Майкрософт).  Дополнительные сведения об изменениях можно найти в [руководстве по DevTools Microsoft Edge](../../devtools-guide/whats-new.md) .

### JavaScript

[EdgeHTML 16 сборок на основе оптимизации производительности в](https://blogs.windows.com/msedgedev/2017/10/31/optimizations-webassembly-sharedarraybuffer-atomics-edgehtml-16/#FodxEPHxR4WkbtyA.97) предыдущих выпусках, разворачивая возможность использования обработчика Chakra для замедленных и повторно заданных функций, используйте кэши с полиморфизмом и оптимизируйте функции с блоками *try/finally* .

Кроме того, функции, предварительно отображаемые в EdgeHTML 15, теперь являются стабильными и включены по умолчанию.

#### Новые функции (по умолчанию)

* [Сборка](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) Обладатель звания MVP ([Demo](https://webassembly.org/demo/))
* [Общая память и атомарные](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

### API запроса на оплату

[API запроса на оплату](../windows-integration/payment-request-api.md) — это открытый стандарт, который позволяет браузерам выступать в качестве посредника между продавцами, получателями и методами оплаты (например, кредитными картами), которые пользователи хранили в облаке.  API-интерфейс в EdgeHTML 16 обновлен в соответствии с последней спецификацией [API запроса на оплату](https://w3c.github.io/payment-request/) W3C. К ним относятся:
* Поддержка `canMakePayment()` метода
* Поддержка `requestId` Свойства
* Поддержка `id` Свойства
* Значение, заданное по умолчанию для `complete()` параметра метода, `result` изменено с "" на "неизвестно"

### Обслуживание сотрудников

[Служебные работники](https://www.w3.org/TR/service-workers-1/) — это управляемые событиями скрипты, которые выполняются в фоновом режиме веб-страницы. ИТ-специалисты включают функции, ранее доступные только для собственных приложений, например перехват и обработку запросов из сети, управление фоновой синхронизацией, локальное хранилище и Push-уведомления. Служба поддержки для сотрудника по-прежнему находится в разработке, но вы можете протестировать ее в Microsoft Edge с помощью нашего экспериментального обслуживания сотрудников службы, включив функцию сотрудника в разделе **about: flags**.

### WebVR
В WebVR для Microsoft Edge добавлена поддержка [контроллеров движения](https://developer.microsoft.com/windows/mixed-reality/motion_controllers). Эти контроллеры имеют точное расположение в пространстве, что позволяет более детально взаимодействовать с цифровыми объектами в Virtual Reality.

![Контроллеры движений](../media/MotionControllers.jpg)

WebVR также был оптимизирован для поддержки двух различных типов взаимодействия.

**Компьютеры с Windows Mixed Reality** — настольные компьютеры и Ноутбуки с интегрированной графикой.  Когда вы подключены к этим устройствам, наши впечатляющие гарнитуры работают в 60 кадров за секунду.  
**Портативные компьютеры с Windows Mixed Reality** — настольные компьютеры и Ноутбуки с отдельными графическими объектами. Когда вы подключены к этим устройствам, наши впечатляющие гарнитуры работают в 90 кадров за секунду.   

Обе настройки будут поддерживать один и тот же впечатляющий видеоролик и игровой интерфейс. 

Дополнительные сведения о предстоящих обновлениях для Windows Mixed Reality можно найти в блоге "обновление праздников для Windows [Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update/) ". 

Руководства и демонстрационные материалы заголовков [руководства разработчика WebVR](https://docs.microsoft.com/microsoft-edge/webvr/).

 > [!NOTE] 
 > Поскольку спецификация WebVR по-прежнему находится на стадии разработки, реализация Microsoft Edge может измениться позже.

## Новые API-интерфейсы в EdgeHTML 16

Ниже приведен полный список новых API-интерфейсов в EdgeHTML 16. Они указаны в формате **[имя интерфейса]. [ Имя API]**.

> [!NOTE] 
> Несмотря на то что в DOM используются следующие API-интерфейсы, поведение некоторых из них может по-прежнему находиться в разработке. Для официального приложения Word о поддержке функций вы можете обратиться к [Microsoft Edge Platform Status](https://developer.microsoft.com/microsoft-edge/platform/status/) .

<iframe height='559' scrolling='no' title='Новые API-интерфейсы в EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Ознакомьтесь с <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> новыми API-интерфейсами в EdgeHTML 16 на </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) на <a href='https://codepen.io'> CodePen </a> .</iframe></p>

<h2 id="previous-edgehtml-releases">Предыдущие выпуски EdgeHTML</h2>
<p><a href="https://aka.ms/devguide_edgehtml_12" data-raw-source="[EdgeHTML 12 / Windows build 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)">EdgeHTML 12/Windows Build 10240 (7/2015)</a>

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

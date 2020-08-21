---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: В этом руководстве представлен обзор функций и стандартов для разработчиков, которые включены в Microsoft Edge.
title: Новые функции и API в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: a15888bc8c1314d61d436759e5d63be942174ea4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941932"
---
# Новые возможности Microsoft EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Ниже перечислены новые и обновленные функции, публикуемые в [веб-платформе Microsoft Edge HTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) в [рамках обновления](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10.10.2017, сборка 16299\).  Сведения об изменениях в конкретных сборках Windows Insider Preview см. в статье ["Изменение журнала изменений Microsoft Edge"](https://developer.microsoft.com/microsoft-edge/platform/changelog) и ["Новые возможности Microsoft EdgeHTML".](../whats-new.md)  

Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md)  

## Новые и обновленные функции  

### Макет сетки CSS  

Теперь Microsoft Edge теперь поддерживает непрефиксированную реализацию макета [CSS.](https://www.w3.org/TR/css-grid-1)  [Макет сетки](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) определяет двумерную систему макета на основе сетки, которая повышает повышает повышенную четкость макета, чем возможно, расположить с помощью плаваток или сценариев.  В примере ниже настроена структура для базовой веб-страницы с помощью макета CSS.  

<iframe height='303' scrolling='no' title='Макет сетки CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>См. <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> сетку пера CSS </a> на mSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> кодировке Кодировки. </a></iframe>  

### Положение объекта CSS  

Поддержка EdgeHTML 16 предлагает поддержку свойств CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) и.  Эти свойства определяют положение и размер замещаемого содержимого в поле содержимого.  

### Средства разработчика  

Этот выпуск был начал рефакторского усилий для оценки и производительности, а также добавили набор новых функций, которые можно приступить к [использованию сборок Windows Insider.](https://insider.windows.com)  Дополнительные сведения об [изменениях можно](../whats-new.md) найти в руководстве по разработчикам Microsoft Edge.  

### JavaScript  

[Сборки EdgeHTML 16 сборки BavaScript 16 с учетом оптимизации предыдущих выпусков JavaScript](https://blogs.windows.com/msedgedev/2017/10/31) путем расширения возможности обработчика функций для отклонения и повторения, использования повторяющихся кэшей и оптимизации функций `try` / `finally` с блоками.  

Кроме того, функции, предварительно увидевшие функции в предварительной версии браузера Microsoft EdgeHTML 15, теперь по умолчанию доступны.  

#### Новые возможности  

Включено по умолчанию  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([демонстрация](https://webassembly.org/demo)\)  
*   [Общие память и атоминцы](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### API запроса оплаты  

[API запросов платежей](../windows-integration/payment-request-api.md) — это открытый aPI-браузера, который позволяет браузерам работать в качестве промежуточного промежуточного предприятия, потребителей и методов оплаты \(например, кредитных карт\).  API в EdgeHTML 16 был обновлен в соответствии с последней [спецификацией API](https://w3c.github.io/payment-request) W3C.  К ним относятся:  

*   Поддержка `canMakePayment()` метода  
*   Поддержка `requestId` свойства  
*   Поддержка `id` свойства  
*   Значение по умолчанию для `complete()` параметра метода `result` изменен с "неизвестно" на "неизвестно"  

### Служебные сценарии  

[Работники служб — это](https://www.w3.org/TR/service-workers-1) сценарии на основании событий, которые выполняются в фоновом режиме веб-страницы.  Сотрудники служб, ранее доступные только с собственными приложениями, такими как перекрестные запросы и обработка запросов из сети, управление фоном и обработкой фонового хранилища, локальное хранилище и push-уведомления.  Поддержка для работника по обслуживанию еще работает над разработкой, но вы можете протестировать поддержку PWA в Microsoft Edge с эксперименальными службами, включив `about:flags` функцию.  

### WebVR  

Приложение WebVR для Microsoft Edge добавила поддержку [контроллеров движения.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)  Эти контроллеры имеют тщательное положение пространства, с помощью которой в виртуальной реальности виртуально подходят для взаимодействия с цифровыми объектами.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Контроллеры перемещения" lightbox="../media/MotionControllers.jpg":::
   Контроллеры перемещения  
:::image-end:::  

Также был оптимизирован веб-виртуал изменений для поддержки двух разных типов возможностей.  

**Компьютеры с Windows Mixed Reality** — настольные компьютеры и ноутбуки с интегрированными графикой.  После установки к этим устройствам наши мелодии гарнитуры будут работать в 60 кадров в секунду.  
**Windows Mixed Reality —** компьютеры и ноутбуки с разными графическими объектами.  После установки к этим устройствам наши иммерсивные гарнитуры будут работать в течение 90 кадров в секунду.  

Обе настройки поддерживают одно и то же взаимодействие с видео и играми.  

Дополнительные сведения о предстоящих обновлениях Windows Mixed Reality см. в записи блога об обновлениях [windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)  

Для направляющей и демонстраций см. руководство [для разработчиков WebVR.](/microsoft-edge/webvr)  

 > [!NOTE] 
 > Так как речь WebVR еще находится в разработке, реализация Microsoft Edge может измениться ниже строки ниже.  

## Новые API в EdgeHTML 16  

Ниже приведен полный список новых aPI в EdgeHTML 16.  Они указаны в `[interface name].[api name]` формате.

> [!NOTE] 
> Хотя в DOM представлены указанные ниже API, конечные советы по могут быть настоящими.  Сведения о  [том, почему официальное слово](https://developer.microsoft.com/microsoft-edge/platform/status) доступно в поддержке функций, см. в статье о состоянии платформы Microsoft Edge.  

---  

<iframe height='559' scrolling='no' title='Новые API в EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>См. раздел <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> "Новый API" в EdgeHTML 16 </a> на MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> коде CodePen. </a></iframe>  

---  

## Предыдущие выпуски EdgeHTML  

[EdgeHTML 12/ Windows сборка 10240 (07.07.2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Windows сборка 10586 (11.11.2015)](./edgehtml-13.md)  

[EdgeHTML 14/ Windows сборка 14393 (8.08.2016)](./edgehtml-14.md)  

[EdgeHTML 15 / Windows сборка 15063 (4.04.2017)](./edgehtml-15.md)  

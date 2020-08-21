---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Узнайте, как С помощью API веб-уведомлений можно разрешить отправку уведомлений пользователям за пределами контекста браузера Microsoft Edge.
title: API веб-уведомлений — руководство по разработке
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 24b8a7b25fb3e0f0221f6d81b105d5d0374ea423
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941800"
---
# API веб-уведомлений  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

API веб-уведомлений позволяет отправлять пользователям уведомления о них за пределами контекста веб-страницы в браузере Microsoft Edge.  Пример использования этой функции в действии может быть вызвано приложением для обмена сообщениями, например Skype.  Когда пользователь получит новое сообщение, на рабочем столе появляется уведомление, сообщающее его об отправке.  Веб-уведомления полностью интегрируются с платформой уведомлений и центром уведомлений в Windows 10.  

## Создание уведомления  

Ниже создается уведомление о мехическом коде, создав объект [уведомления](https://msdn.microsoft.com/library/mt710818) [с](https://msdn.microsoft.com/library/mt710826)заголовком, [значком](https://msdn.microsoft.com/library/mt710814)и [набором](https://msdn.microsoft.com/library/mt710811) параметров текста:  

<iframe height='295' scrolling='no' title='веб-уведомления' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Просматривайте <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> веб-уведомления </a> к аркету с помощью документов на Microsoft Edge <a href='https://codepen.io/MicrosoftEdgeDocumentation'> </a> (@MicrosoftEdgeDocumentation) на <a href='https://codepen.io'> кодировке </a> кода.</iframe>  

Настоятельно рекомендуется использовать **значок** для каждого уведомления.  Это позволит улучшить уведомление только от точки пользовательского пользовательского пользовательского пользовательского сайта, но и оповещать пользователей о том, с каких лицензий отправляется уведомление.  

Просмотрите видеоролик ниже, чтобы узнать, как создавать веб-уведомления, и узнать, как это работает в Windows 10!  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### Свойства уведомления  

Уведомления можно настроить следующими свойствами:  

:::row:::
   :::column span="1":::
      [body](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      Текст уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [dir](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      Направление текста уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [icon](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      URL-адрес уведомления, используемый для значка своего значка.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [ланг](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      Язык уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [разрешение](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      В текущем уведомлении отображается разрешение, предоставленное пользователю для текущего оригинала.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [tag](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      Тег уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [title](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      Название уведомления.  
   :::column-end:::
:::row-end:::  

### События уведомлений  

Следующие события используются в объекте [уведомления:](https://developer.mozilla.org/docs/Web/API/Notification)  

:::row:::
   :::column span="1":::
      [onclick](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      Выбирайте уведомление, нажав ширину.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onclose](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      Получайте уведомления, когда пользователь закрывает уведомление или автоматические ожидания.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onerror](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      Исчезновение ошибки при обработке уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onshow](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      Появляются уведомления.  
   :::column-end:::
:::row-end:::  

### Способы уведомлений  

В объекте Уведомления можно использовать [следующие](https://developer.mozilla.org/docs/Web/API/Notification) способы:  

:::row:::
   :::column span="1":::
      [close](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      Закрывает отображаемое уведомление.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [запросразрешения](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      Запросы на разрешение пользователя, позволяющие разрешить отображение уведомлений текущим оригиналом.  
   :::column-end:::
:::row-end:::  

## Разрешения для уведомлений  

Microsoft Edge позволяет пользователям управлять разрешениями для каждого отдельного домена веб-сайтов.  При появлении сообщения о **Yes** том, что в домене потребуется выбрать "Да" **или "Нет".**  [Метод запроса Permission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) (сигнал из-за параметров разрешений) используется для сигнала в состоянии разрешений. `granted` `denied` `default`  Значение указывает на то, что пользователь не принял `default` решение, которое видно как эквивалент. `denied`  

## Справочные материалы по API  

[Веб-уведомления](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## Спецификаци  

[Веб-уведомления](https://notifications.spec.whatwg.org)  

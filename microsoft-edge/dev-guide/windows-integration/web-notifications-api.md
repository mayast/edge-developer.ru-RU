---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Сведения о том, как можно использовать API веб-уведомлений, чтобы разрешить веб-сайтам отправлять уведомления пользователей за пределами контекста браузера Microsoft Edge.
title: 'Руководство для разработчиков: API веб-уведомлений'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/18/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: da563a333491ef699925adec6f97b3c21d3e54a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571239"
---
# API веб-уведомлений

API веб-уведомлений позволяет веб-сайтам отправлять уведомления пользователей за пределами контекста веб-страницы в браузере Microsoft Edge. Примером этой функции в действии может быть приложение для обмена сообщениями, например Skype. Когда пользователь получит новое сообщение, на его рабочем столе появится уведомление о сообщении. Веб-уведомления полностью интегрированы с платформой уведомлений и центром действий в Windows 10. 

## Создание уведомления

На CodePen рисунке ниже показано, как создать фиктивное уведомление Skype, сделав [`Notification`](https://msdn.microsoft.com/library/mt710818) объект с [`title`](https://msdn.microsoft.com/library/mt710826) [`icon`](https://msdn.microsoft.com/library/mt710814) [`body`](https://msdn.microsoft.com/library/mt710811) установленным флажком "и".


<iframe height='295' scrolling='no' title='Веб-уведомления' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> с веб-уведомлениями о перьях </a> по Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) на <a href='https://codepen.io'> CodePen </a> .
</iframe>

Настоятельно рекомендуется `icon` указывать для каждого уведомления. Это не только улучшит уведомления с точки зрения пользовательского интерфейса, но и позволяет оповещать пользователей о том, где отправляются уведомления.

Посмотрите видеоролик ниже, в котором показано, как создать веб-оповещение и узнать, как это происходит в Windows 10.


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### Свойства уведомлений

Уведомления можно настроить с помощью следующих параметров:

Свойство | Описание
:-------- | :----------
[body](https://msdn.microsoft.com/library/mt710811) | Основной текст уведомления.
[dir](https://msdn.microsoft.com/library/mt710813) | Направление текста уведомления.
[icon](https://msdn.microsoft.com/library/mt710814) | URL-адрес уведомления, который используется для его значка.
[файл](https://msdn.microsoft.com/library/mt710815) | Язык уведомления.
[PermissionSet](https://msdn.microsoft.com/library/mt670637) | Текущее разрешение на отображение уведомления, предоставленное пользователем для текущего происхождения.
[tag](https://msdn.microsoft.com/library/mt710825) | Тег уведомления.
[title](https://msdn.microsoft.com/library/mt710826) | Название уведомления.

### События уведомления

С объектом используются следующие события [`Notification`](https://msdn.microsoft.com/library/mt710818) :

Событие | Описание
:-------- | :----------
[OnClick](https://msdn.microsoft.com/library/mt712180) | Активируется при щелчке уведомления пользователем.
[OnClose (закрыть)](https://msdn.microsoft.com/library/mt712178) | Активируется при закрытии уведомления пользователем или автоматическим тайм-аутам.
[ПриОшибке](https://msdn.microsoft.com/library/mt712181) | Активируется при возникновении ошибки при обработке уведомления.
[onShow](https://msdn.microsoft.com/library/mt712182) | Активируется при отображении уведомления.

### Способы уведомления

С объектом используются следующие методы [`Notification`](https://msdn.microsoft.com/library/mt710818) :

Метод | Описание
:-------- | :----------
[close](https://msdn.microsoft.com/library/mt670636) | Закрывает открытое уведомление.
[requestPermission](https://msdn.microsoft.com/library/mt710824) | Запрашивает разрешение от пользователя, чтобы разрешить отображение уведомлений текущим источником.

## Разрешения для уведомлений

Microsoft EDGE позволяет пользователям управлять разрешениями уведомлений для каждого определенного домена веб-сайта. Вы можете выбрать вариант "Да" или "нет" при появлении запроса от домена, чтобы позволить ему показывать уведомления. [`requestPermission`](https://msdn.microsoft.com/library/mt710824)Метод используется, чтобы сообщить состояние разрешения как `granted` , так `denied` и `default` . Значение указывает на то `default` , что пользователь не принял решение, которое рассматривается как эквивалент `denied` .




## Справочные материалы по API

[Веб-уведомления](https://msdn.microsoft.com/library/mt710827)

## Specification

[Веб-уведомления](https://notifications.spec.whatwg.org)

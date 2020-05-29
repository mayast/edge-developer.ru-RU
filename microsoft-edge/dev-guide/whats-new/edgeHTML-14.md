---
description: На этой странице представлены общие сведения о новых возможностях EdgeHTML 14.
title: Новые возможности EdgeHTML 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: 5e9e0d5d9a53c5ecbfeb4b93c3b453a3d2904e2b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570922"
---
# Новые возможности EdgeHTML 14
Ниже приведены изменения, которые поставляются с EdgeHTML 14 по [обновлению годовщины Windows 10](https://blogs.windows.com/windowsexperience/2016/06/29/windows-10-anniversary-update-available-august-2/) (08/2016, сборка 14393). Общие сведения об изменениях, внесенных в общий браузер Microsoft EDGE, приведены в [статье Введение в EdgeHTML 14 с помощью обновления годовщины Windows 10](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14).

Ниже приведен список постоянных [https://aka.ms/devguide_edgehtml_14](https://aka.ms/devguide_edgehtml_14) изменений.

## Новые возможности

### Расширения
Расширения — это небольшие программы, которые можно использовать для добавления новых функций в Microsoft EDGE или изменения существующих функций. Расширения предназначены для того, чтобы улучшить работу с повседневным просмотром пользователя, предоставив специализированные функциональность, важную для целевых аудиторий. Microsoft EDGE поддерживает новую модель расширения на основе HTML, JavaScript и CSS. Эта новая модель совместима с коллегами, что означает, что существующие разработчики расширений Chrome смогут переносить свои расширения в Microsoft Edge с минимальными изменениями. Дополнительные сведения можно найти в документах для разработчиков [расширений Microsoft Edge](https://docs.microsoft.com/microsoft-edge/extensions) . 

### API выборки
[API FETCH](https://fetch.spec.whatwg.org/#fetch-api) использует `fetch` метод для выборки ресурсов. В прошлом это было достигнуто `XMLHttpRequest` . Выбор не только упрощает использование, но и предоставляет доступ к запросам и ответам более низким уровней. Ознакомьтесь с дополнительными сведениями о API выборки в записи блога Microsoft EDGE, [fetch (или неограниченные ограничения XHR)](https://blogs.windows.com/msedgedev/2016/05/24/fetch-and-xhr-limitations/).

### JavaScript

EdgeHTML 14 предоставляет ряд новых и экспериментальных функций для Chakra, Microsoft Edge Powering модуля JavaScript:

#### Новые функции (по умолчанию)

* [Параметры по умолчанию](https://developer.microsoft.com/microsoft-edge/platform/status/defaultparameteres6) (ES2015)
* [Оператор возведения](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016) в степень (ES2016)
* [Array. prototype. включает](https://developer.microsoft.com/microsoft-edge/platform/status/arrayprototypeincludeses2016) (ES2016)
* [Object. valuess](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/values) и [Object.](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) in (ES2017)

#### Экспериментальные функции JavaScript (включены с *флагами about: flags*)

* [Модули](https://blogs.windows.com/msedgedev/2016/05/17/es6-modules-and-beyond/) (ES2015)
* [Async/await](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctionses2016) (ES2017)
* [Символы регулярных выражений](https://developer.microsoft.com/microsoft-edge/platform/status/regexpbuiltinses6) (ES2015)

Для получения дополнительных сведений изучите [*Предварительный просмотр модулей ES6 и многое другое из ES2015, ES2016 и более поздних*](https://blogs.windows.com/msedgedev/2016/05/17/es6-modules-and-beyond/) и [*асинхронных кодов, более простой доступ к ES2016 функциям асинхронных функций в Chakra и Microsoft Edge*](https://blogs.windows.com/msedgedev/2015/09/30/asynchronous-code-gets-easier-with-es2016-async-function-support-in-chakra-and-microsoft-edge/).

### API проверки подлинности веб-сайта (FIDO 2,0 Web API)
API проверки подлинности (прежнее название — FIDO 2,0) в Microsoft EDGE позволяет веб-приложениям использовать биометрию [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) для проверки подлинности пользователя, чтобы пользователи могли избежать проблем и рисков управления паролями, включая подбор пароля, фишинг и атаки Keylogging. Текущая реализация Microsoft EDGE (предварительно фиксированная версия) основана на более ранней версии спецификации веб-проверки подлинности и, как правило, изменяется в будущем. Подробнее о веб-проверке подлинности: [веб-аутентификация и Windows Hello](https://docs.microsoft.com/microsoft-edge/dev-guide/device/web-authentication).

### Веб-уведомления
С помощью веб-уведомлений сайты должны отображать уведомления о том, что пользователи находятся за пределами контекста веб-страницы и браузера, которые сообщают пользователям о новых сообщениях, оповещениях и о том, чтобы сайты могли повышать участие пользователей. Веб-уведомления в Microsoft Edge полностью интегрированы с платформой уведомлений и центром обработки в Windows 10, обеспечивая единообразную работу с другими приложениями в системе и простое управление разрешениями и беззвучными часами. Для получения дополнительных сведений просмотрите [веб-уведомления в Microsoft Edge](https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge/) . 

### Веб-интерфейс голосовых функций
[API для веб-речи](https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html) — это API JavaScript, состоящий из двух частей: распознавание речи и синтез речи (или текст в речь). В настоящее время Microsoft EDGE поддерживает только синтез речи. Синтез речи состоит из преобразования текста в речь, который пользователь слышит через динамики. Ознакомьтесь со статьей "речь" для разработчиков для получения дополнительной информации в Интернете: руководство по разработке [синтеза речи](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/web-speech-api) . 

## Новые API-интерфейсы в EdgeHTML 14

Ниже приведен полный список новых API-интерфейсов в EdgeHTML 14. Они указаны в формате **[имя интерфейса]. [ Имя API]**.
<iframe height='585' scrolling='no' title='Новые API-интерфейсы в EdgeHTML 14' src='//codepen.io/MSEdgeDev/embed/oWMEPE/?height=585&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь с <a href='https://codepen.io/MSEdgeDev/pen/oWMEPE/'> новыми API-интерфейсами для EdgeHTML 14 на </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) в <a href='https://codepen.io'> CodePen </a> .
</iframe>

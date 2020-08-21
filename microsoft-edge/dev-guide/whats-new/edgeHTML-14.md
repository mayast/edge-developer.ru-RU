---
description: На этой странице представлен обзор новых возможностей Браузера Microsoft EdgeHTML 14.
title: Новые функции и API в EdgeHTML 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 7f3fcbbf84873fbf0851e1652bde48632e6c4378
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941908"
---
# Новые возможности в Microsoft EdgeHTML 14  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Ниже перечислены изменения, публикуемые [вместе](https://blogs.windows.com/windowsexperience/2016/06/29) с EdgeHTML 14 в себе после установки юбилейного обновления \(08.08.2016, сборка 14393\).  Обзор изменений общего браузера Microsoft Edge см. в руководстве пользователя Microsoft [Edge 14 с юбилейным обновлением Windows 10.](https://blogs.windows.com/msedgedev/2016/08/04)  

Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_14](./edgehtml-14.md)  

## Новые возможности  

### Расширения  

Расширения — это небольшие программы, которые можно использовать для добавления новых функций в Microsoft Edge или изменения существующих.  Расширения предназначены для улучшения просмотра пользователей, предусматривая целевую аудиторию функциональность, которая важна для целевой аудитории.  Microsoft Edge поддерживает новые модели расширения на основе HTML, JavaScript и CSS.  Эта новая модель совместима с Chrome, то есть разработчики расширений Chrome смогут перенести свои расширения в Microsoft Edge с минимальными изменениями.  Дополнительные сведения см. в [документах](../../extensions/index.md) разработчиков Microsoft Edge.  

### Fetch API  
[API для получения](https://fetch.spec.whatwg.org#fetch-api) ресурсов улучшает метод `fetch` получения доступа к API.  В раннем случае это была достижена. `XMLHttpRequest`  Упрощен лишь обычный доступ, она также обеспечивает более низкий доступ к запросам и ответам.  Дополнительные сведения об API удаленного доступа в записи блога Microsoft Edge, удаленном [французском (или неограниченных ограничениях XHR).](https://blogs.windows.com/msedgedev/2016/05/24)  

### JavaScript  

EdgeHTML 14 предлагает ряд новых и экспертальных возможностей в Шкмолу, модуль JavaScript.  

#### Новые возможности  

Включено по умолчанию  

*   [Параметры](https://developer.microsoft.com/microsoft-edge/platform/status/defaultparameteres6) по умолчанию \(ES2015\)
*   [Оператор экспоненциального оператора](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016) \(ES2016\)
*   [Array.prototype.includes](https://developer.microsoft.com/microsoft-edge/platform/status/arrayprototypeincludeses2016) \(ES2016\)
*   [Object.values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/values) и [object.entries](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) \(ES2017\)  

#### Экспертные функции JavaScript  

Доступно с `about:flags`  

*   [Modules](https://blogs.windows.com/msedgedev/2016/05/17) \(ES2015\)  
*   [Async/await](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctionses2016) \(ES2017\)  
*   [Символы regex](https://developer.microsoft.com/microsoft-edge/platform/status/regexpbuiltinses6) \(ES2015\)  

Для получения дополнительных сведений ознакомьтесь с этой функцией, которая представляет [собой es2015, ES2016 и более](https://blogs.windows.com/msedgedev/2016/05/17) высокий и асинхронный и асинхронный код, упрощают поддержку [функций ES2016 в Chakra и Microsoft Edge.](https://blogs.windows.com/msedgedev/2015/09/30)  

### API веб-проверки подлинности веб-проверки  

Веб-API FIDO 2.0  

API веб-службы Подлинности \(прежнее имя — FIDO 2.0\) позволяет веб-приложениям использовать биоометрические показатели [Windows Hello,](https://www.microsoft.com/windows/comprehensive-security) чтобы избежать рисков и рисков управления паролями, включая рекомендации по управлению паролями, фишинговыми и ключевыми словами.  Текущая реализация Microsoft Edge \( `ms-` префикс\) основана на более ранней черновике спецификации веб-проверки подлинности и, скорее всего, изменится.  Подробнее о веб-проверке подлинности: [веб-проверка подлинности и Windows Hello.](../windows-integration/web-authentication.md)

### Веб-уведомления
Веб-уведомления позволяют пользователям отображать уведомления о появлении уведомлений пользователям за пределами контекста веб-страницы и браузера, чтобы пользователи знали о новых сообщениях и оповещениях и позволяя использовать сайты для улучшения взаимодействия пользователей.  Веб-уведомления в Microsoft Edge полностью интегрированы со платформой уведомлений и центром уведомлений в Windows 10, что упрощает работу с другими приложениями в системе и удобный управление разрешениями и "Не беспокоить".  Дополнительные [сведения см. в веб-уведомлениях в Microsoft Edge.](https://blogs.windows.com/msedgedev/2016/05/16)  

### Web Speech API
[API Web Speech — это API](https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html) JavaScript JavaScript, представляемый из двух частей: распознавание речи и речи синтаксис "\(или текст в речь\).)  В настоящее время Microsoft Edge поддерживает только синонимы речи.  Синонимы речи приводят к преобразованию текста в речь, которая воспроизводит пользователь слышите их.  Дополнительные сведения [см. в статье "Веб-речь:](https://developer.mozilla.org/docs/Web/API/Web_Speech_API) речь для разработчика "Речи для разработчиков": "Руководство по синтаксису разработчику" для разработчиков.  

## Новый API в Microsoft EdgeHTML 14

Ниже приведен полный список новых aPI в Microsoft EdgeHTML 14.  Они указаны в `[interface name].[api name]` формате.  

<iframe height='585' scrolling='no' title='Новый API в Microsoft EdgeHTML 14' src='//codepen.io/MSEdgeDev/embed/oWMEPE/?height=585&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. раздел <a href='https://codepen.io/MSEdgeDev/pen/oWMEPE/'> "Новый API" в EdgeHTML 14 </a> на MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> коде CodePen. </a></iframe>  

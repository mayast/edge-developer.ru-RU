---
description: Общие сведения об изменениях высокого влияния, которые могут повлиять на совместимость сайтов
title: 'Совместимость сайта: влияние на изменения, которые поступают в Microsoft Edge'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, совместимость, веб-платформа
ms.openlocfilehash: 0785544d0245827f58f3f7c71edd5a18a3d12404
ms.sourcegitcommit: d982699ee25e8704fcaad7a15b4d8d015aef2f12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/14/2020
ms.locfileid: "10868767"
---
# Совместимость сайта: влияние на изменения, которые поступают в Microsoft Edge  

Интернет постоянно развивается, чтобы улучшить взаимодействие с пользователем, безопасность и конфиденциальность.  В некоторых случаях изменения могут значительно повлиять на функциональность существующих страниц.  В таблице ниже сведены некоторые изменения, которые в настоящее время отслеживают сотрудники Microsoft Edge.  Регулярно проверяйте обратно. Группа Microsoft Edge обновляет следующую страницу в соответствии с обдумыванием эволюции, временные шкалы solidify и новые изменения объявляются.  

| Изменение | Канал Stable | Эксперименты | Дополнительные сведения |  
|:--- |:--- |:--- |:--- |
| Файлы cookie по умолчанию для `SameSite=Lax` | [Chrome или Chrome + 1](#release-comments)  | Канарские V82, dev V82 | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, проверьте [запись состояния платформы Chrome][ChromePlatformStatus5088147346030592].  |  
| Политика для ссылки на источник: по умолчанию `strict-origin-when-cross-origin` | [Chrome или Chrome + 1](#release-comments)  | Канарские V79, dev V79 | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, проверьте [запись состояния платформы Chrome][ChromePlatformStatus6251880185331712].  |  
| Запрет синхронного объекта XmlHttpRequest при закрытии страницы | [Хром + 1](#release-comments) \ (Edge v83 \) |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Соответствующий хром Microsoft Edge предложит групповую политику, чтобы отключить это изменение до пограничного V88.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, проверьте [запись состояния платформы Chrome][ChromePlatformStatus4664843055398912].  |  
| Вывод неявных запросов на запросы разрешений на уведомления | Пограничный v84 |  | В ответ на запрос уведомлений в тихом окне отображается слабый значок запроса для разрешений на уведомления о сайтах, запрашиваемых с помощью интерфейса `Notifications` или `Push` API, заменяя полный или стандартный пользовательский интерфейс подсказки для всплывающих подсказок.  В настоящее время эта функция включена для всех пользователей.  Чтобы отказаться от запросов на уведомления в тихом режиме, перейдите на `edge://settings/content/notifications` .  В будущем группа Microsoft Edge может проанализировать повторное включение полного всплывающего уведомления в некоторых сценариях.  |  
| Отключение TLS/1.0 и TLS/1.1 по умолчанию | Пограничный v84 |  | Для выяснения воздействия на веб-сайты вы можете установить `edge://flags/#display-legacy-tls-warnings` флажок, чтобы при загрузке страниц, требующих устаревших протоколов TLS, выводилось сообщение о небезопасном использовании Microsoft Edge.  Групповая политика [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] разрешает повторное включение TLS/1.0 и TLS/1.1; После появления 88 эта политика останется доступной.  |  
| Блокировка загрузки смешанного содержимого | [Хром + 1](#release-comments) \ (Edge V86 \)  |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, ознакомьтесь с [записью блога безопасности Google][GoogleBlogSecurity20200206].  Расписание выпуска Microsoft для типов файлов, которые нужно предупреждать или блокировать, планируется для одного выхода после Chrome.  |  
| Устаревшие AppCache | [Хром + 1](#release-comments) \ (Edge V86 \)  |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Дополнительную информацию можно узнать в [документации по WebDev][WebDevAppCacheRemoval].  Расписание выпуска Microsoft для устаревшей планируется для одного выпуска после Chrome.  Запрос [маркера AppCache OriginTrial][AppCacheOriginTrial] позволяет сайтам продолжать использовать устаревший API, пока не появится Edge V90.  |  
| Удаление Adobe Flash | Пограничный V88  |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Для получения дополнительной информации ознакомьтесь с [РазChromiumной схемой Adobe Flash][ChromiumFlashRoadmapSupportRemoved].  | 
##### Примечания о выпуске  

:::row:::
   :::column span="1":::
      Chrome + 1
   :::column-end:::
   :::column span="2":::
      На основе отзывов пользователей и разработчиков указанные функции или изменения отставляются один выпуск после Chrome.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome или Chrome + 1
   :::column-end:::
   :::column span="2":::
      На основе отзывов пользователей и разработчиков указанные функции или изменения поставляются одновременно или одним выпуском после Chrome.
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-Policies | Документы Microsoft"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Отключить синхронизацию XHR при закрытии страницы JavaScript | Состояние платформы Chrome"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Файлы cookie по умолчанию SameSite = слабый | Состояние платформы Chrome"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Политика "источник ссылки": по умолчанию используется строгое происхождение Состояние платформы Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Поддержка флэш-памяти, удаленная из Chromium (targets: Chrome 88 +-Янв 2021)-Flash-схема | Проекты Chromium"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Защита пользователей от небезопасных Скачиваний в Google Chrome-блоге по безопасности Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal/ "Удаление AppCache"
[AppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Маркер AppCache OriginTrial"

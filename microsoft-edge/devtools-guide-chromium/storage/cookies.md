---
description: Сведения о том, как просматривать, изменять и удалять файлы cookie HTTP для страницы с помощью Microsoft Edge DevTools.
title: Просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: eaaf4663504fc674fd70dc1ca9e0357febb529e0
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993242"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools  

[Cookie-файлы HTTP][MDNHTTPCookies] преимущественно используются для управления сеансами пользователей, хранения параметров персонализации пользователей и отслеживания поведения пользователей.  Файлы cookie — это также причина, по которой на этой странице используются формы разрешения файлов cookie, которые вы видите в Интернете.  В приведенном ниже руководстве объясняется, как просматривать, изменять и удалять cookie-файлы HTTP для страницы с [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Открытие области "файлы cookie"  

1.  [Откройте DevTools][DevToolsOpen].  
1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Откроется область **манифеста** .  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Рисунок 1: область манифеста  
    :::image-end:::  

1.  В разделе **хранилище** разверните **cookie-файлы**, а затем выберите источник.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Область «cookies»" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Рисунок 2: область "cookie"  
    :::image-end:::  

## Поля  

Таблица **cookies** включает в себя указанные ниже поля.  

*   **Имя**.  Имя cookie-файла.  
*   **Value (значение**).  Значение cookie-файла.  
*   **Domain (домен**).  Узлы, которым разрешено принимать cookie-файлы.  Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].  
*   **Path (путь**).  URL-адрес, который должен существовать в запрашиваемом URL-адресе, чтобы отправить `Cookie` заголовок.  Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].  
*   **Истекает/Макс-возраст**.  Дата окончания срока действия или максимальный возраст cookie-файла.  Просмотр [постоянных файлов cookie][MDNHTTPCookiesPermanent].  Для [cookie-файлов сеанса][MDNHTTPCookiesSession] это значение всегда `Session` .  
*   **Размер**.  Размер cookie-файла (в байтах).  
*   **Http**.  Если значение равно true, это поле указывает на то, что файл cookie следует использовать только по протоколу HTTP и не может быть изменен на JavaScript.  Просмотр [файлов cookie для HttpOnly][MDNHTTPCookiesSecure].  
*   **Безопасность**.  Если значение равно true, это поле указывает на то, что файл cookie должен быть отправлен на сервер только через безопасное HTTPS-соединение.  Просмотр [защищенных файлов cookie][MDNHTTPCookiesSecure].  
*   **SameSite**.  Содержит `strict` или `lax` Если объект cookie использует экспериментальный атрибут [SameSite][MDNHTTPCookiesSamesite] .  
*   **Priority (приоритет**).  Contains `low` , `medium` \ (по умолчанию \) или, `high` Если cookie использует устаревший атрибут [приоритета cookie-файлов][ChromiumIssue232693] .

## Фильтрация файлов cookie  

Используйте текстовое поле " **Фильтр** " для фильтрации файлов cookie по **имени** или **значению**.  Фильтрация по другим полям не поддерживается.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Фильтрация файлов cookie, которые не содержат идентификатор текста" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Рис. 3: Фильтрация файлов cookie, которые не содержат текст `ID`  
:::image-end:::  

## Изменение файла cookie  

Поля « **имя**», « **значение**», « **домен**», « **путь**» и « **срок действия/максимум»** можно редактировать.  
Дважды щелкните поле, чтобы изменить его.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Присвоение имени файла cookie DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Рисунок 4: Задание имени файла cookie `DEVTOOLS!`  
:::image-end:::  

## Удаление файлов cookie  

Выберите файл cookie и выберите пункт **Удалить выбранное** ![ удаление, ][ImageDeleteIcon]  чтобы удалить определенный файл cookie.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Удаление определенного файла cookie" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Рисунок 5: удаление определенного файла cookie  
:::image-end:::  

**Clear All** ![ ][ImageClearIcon] Чтобы удалить все файлы cookie, выберите Очистить все очистить все.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Удаление всех файлов cookie" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Рисунок 6: Очистка всех cookie-файлов  
:::image-end:::  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Открыть Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Chromium дата_выпуска 232693: реализация поля приоритета для cookie-файлов | Ошибки Chromium"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookie-файлы HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookie-файлы HTTP: постоянные cookie-файлы | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookie-файлы HTTP — SameSite cookie-файлы | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookie-файлы HTTP — область "cookie" | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookie-файлы HTTP — безопасные и HttpOnly cookie-файлы | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookie-файлы HTTP: файлы cookie-сеансов | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

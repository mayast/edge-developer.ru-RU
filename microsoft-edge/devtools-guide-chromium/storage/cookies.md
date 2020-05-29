---
title: Просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 084c4116cd4c9c5e70b2fe341257fa68ba2c8ae7
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612070"
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

  

[Cookie-файлы HTTP][MDNHTTPCookies] преимущественно используются для управления сеансами пользователей, хранения параметров персонализации пользователей и отслеживания поведения пользователей.  Они также являются причиной того, что все эти нежелательные "Эта страница использует файлы" cookie ", которые вы видите в Интернете.  В этом руководстве рассказывается о том, как просматривать, изменять и удалять cookie-файлы HTTP для страницы с [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Открытие области "файлы cookie"   

1.  [Откройте DevTools][DevToolsOpen].  
1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Откроется область **манифеста** .  
    
    > ##### Рис. 1  
    > Область «манифест»  
    > ![Область «манифест»][ImageManifest]  

1.  В разделе **хранилище** разверните **cookie-файлы**, а затем выберите источник.  
    
    > ##### Рисунок 2  
    > Область «cookies»  
    > ![Область «cookies»][ImageCookies]  

## Поля   

Таблица **cookies** включает следующие поля:  

*   **Имя**.  Имя cookie-файла.  
*   **Value (значение**).  Значение cookie-файла.  
*   **Domain (домен**).  Узлы, которым разрешено принимать cookie-файлы.  Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].  
*   **Path (путь**).  URL-адрес, который должен существовать в запрашиваемом URL-адресе, чтобы отправить `Cookie` заголовок.  Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].  
*   **Истекает/Макс-возраст**.  Дата окончания срока действия или максимальный возраст cookie-файла.  Просмотр [постоянных файлов cookie][MDNHTTPCookiesPermanent].  Для [cookie-файлов сеанса][MDNHTTPCookiesSession] это значение всегда `Session` .  
*   **Размер**.  Размер cookie-файла (в байтах).  
*   **Http**.  Если значение равно true, это поле указывает на то, что файл cookie следует использовать только по протоколу HTTP и не может быть изменен на JavaScript.  Просмотр [файлов cookie для HttpOnly][MDNHTTPCookiesSecure].  
*   **Безопасность**.  Если значение равно true, это поле указывает на то, что файл cookie должен быть отправлен на сервер только через безопасное HTTPS-соединение.  Просмотр [защищенных файлов cookie][MDNHTTPCookiesSecure].  
*   **SameSite**.  Содержит `strict` или `lax` Если объект cookie использует экспериментальный атрибут [SameSite][MDNHTTPCookiesSamesite] .  

## Фильтрация файлов cookie   

Используйте текстовое поле " **Фильтр** " для фильтрации файлов cookie по **имени** или **значению**.  Фильтрация по другим полям не поддерживается.  

> ##### Рисунок3  
> Фильтрация файлов cookie, которые не содержат текст `ID`  
> ![Фильтрация файлов cookie, которые не содержат идентификатор текста][ImageCookiesFilter]  

## Изменение файла cookie   

Поля « **имя**», « **значение**», « **домен**», « **путь**» и « **срок действия/максимум»** можно редактировать.  
Дважды щелкните поле, чтобы изменить его.  

> ##### Рисунок4  
> Установка имени файла cookie `DEVTOOLS!`  
> ![Присвоение имени файла cookie DEVTOOLS!][ImageEditCookie]  

## Удаление файлов cookie   

Выберите нужный файл, а затем нажмите кнопку **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] , чтобы удалить один файл cookie.  

> ##### Рисунок 5  
> Удаление определенного файла cookie  
> ![Удаление определенного файла cookie][ImageDeleteCookie]  

**Clear All** ![ ][ImageClearIcon] Чтобы удалить все файлы cookie, выберите Очистить все очистить все.  

> ##### Рисунок6  
> Удаление всех файлов cookie  
> ![Удаление всех файлов cookie][ImageClearAllCookies]  

<!--    -->  

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Рисунок 1: область манифеста"  
[ImageCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-selected.msft.png "Рисунок 2: область "cookie""  
[ImageCookiesFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-filter-id.msft.png "Рис. 3: Фильтрация файлов cookie, которые не содержат идентификатор текста"  
[ImageEditCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-rename.msft.png "Рисунок 4: Установка имени файла cookie в DEVTOOLS!"  
[ImageDeleteCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-delete-selected.msft.png "Рисунок 5: удаление определенного файла cookie"  
[ImageClearAllCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-clear-all.msft.png "Рисунок 6: Очистка всех cookie-файлов"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Открыть Microsoft Edge DevTools"  

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

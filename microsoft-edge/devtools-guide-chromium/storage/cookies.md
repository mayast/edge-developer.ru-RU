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





# <span data-ttu-id="3d867-103">Просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3d867-103">View, Edit, And Delete Cookies With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="3d867-104">[Cookie-файлы HTTP][MDNHTTPCookies] преимущественно используются для управления сеансами пользователей, хранения параметров персонализации пользователей и отслеживания поведения пользователей.</span><span class="sxs-lookup"><span data-stu-id="3d867-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="3d867-105">Они также являются причиной того, что все эти нежелательные "Эта страница использует файлы" cookie ", которые вы видите в Интернете.</span><span class="sxs-lookup"><span data-stu-id="3d867-105">They are also the cause of all of those annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="3d867-106">В этом руководстве рассказывается о том, как просматривать, изменять и удалять cookie-файлы HTTP для страницы с [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="3d867-106">This guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="3d867-107">Открытие области "файлы cookie"</span><span class="sxs-lookup"><span data-stu-id="3d867-107">Open the Cookies pane</span></span>   

1.  <span data-ttu-id="3d867-108">[Откройте DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="3d867-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="3d867-109">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="3d867-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="3d867-110">Откроется область **манифеста** .</span><span class="sxs-lookup"><span data-stu-id="3d867-110">The **Manifest** pane should open.</span></span>  
    
    > ##### <span data-ttu-id="3d867-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="3d867-111">Figure 1</span></span>  
    > <span data-ttu-id="3d867-112">Область «манифест»</span><span class="sxs-lookup"><span data-stu-id="3d867-112">The Manifest pane</span></span>  
    > ![Область «манифест»][ImageManifest]  

1.  <span data-ttu-id="3d867-114">В разделе **хранилище** разверните **cookie-файлы**, а затем выберите источник.</span><span class="sxs-lookup"><span data-stu-id="3d867-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    > ##### <span data-ttu-id="3d867-115">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="3d867-115">Figure 2</span></span>  
    > <span data-ttu-id="3d867-116">Область «cookies»</span><span class="sxs-lookup"><span data-stu-id="3d867-116">The Cookies pane</span></span>  
    > ![Область «cookies»][ImageCookies]  

## <span data-ttu-id="3d867-118">Поля</span><span class="sxs-lookup"><span data-stu-id="3d867-118">Fields</span></span>   

<span data-ttu-id="3d867-119">Таблица **cookies** включает следующие поля:</span><span class="sxs-lookup"><span data-stu-id="3d867-119">The **Cookies** table contains the following fields:</span></span>  

*   <span data-ttu-id="3d867-120">**Имя**.</span><span class="sxs-lookup"><span data-stu-id="3d867-120">**Name**.</span></span>  <span data-ttu-id="3d867-121">Имя cookie-файла.</span><span class="sxs-lookup"><span data-stu-id="3d867-121">The name of the cookie.</span></span>  
*   <span data-ttu-id="3d867-122">**Value (значение**).</span><span class="sxs-lookup"><span data-stu-id="3d867-122">**Value**.</span></span>  <span data-ttu-id="3d867-123">Значение cookie-файла.</span><span class="sxs-lookup"><span data-stu-id="3d867-123">The value of the cookie.</span></span>  
*   <span data-ttu-id="3d867-124">**Domain (домен**).</span><span class="sxs-lookup"><span data-stu-id="3d867-124">**Domain**.</span></span>  <span data-ttu-id="3d867-125">Узлы, которым разрешено принимать cookie-файлы.</span><span class="sxs-lookup"><span data-stu-id="3d867-125">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="3d867-126">Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="3d867-126">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="3d867-127">**Path (путь**).</span><span class="sxs-lookup"><span data-stu-id="3d867-127">**Path**.</span></span>  <span data-ttu-id="3d867-128">URL-адрес, который должен существовать в запрашиваемом URL-адресе, чтобы отправить `Cookie` заголовок.</span><span class="sxs-lookup"><span data-stu-id="3d867-128">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="3d867-129">Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="3d867-129">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="3d867-130">**Истекает/Макс-возраст**.</span><span class="sxs-lookup"><span data-stu-id="3d867-130">**Expires / Max-Age**.</span></span>  <span data-ttu-id="3d867-131">Дата окончания срока действия или максимальный возраст cookie-файла.</span><span class="sxs-lookup"><span data-stu-id="3d867-131">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="3d867-132">Просмотр [постоянных файлов cookie][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="3d867-132">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="3d867-133">Для [cookie-файлов сеанса][MDNHTTPCookiesSession] это значение всегда `Session` .</span><span class="sxs-lookup"><span data-stu-id="3d867-133">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="3d867-134">**Размер**.</span><span class="sxs-lookup"><span data-stu-id="3d867-134">**Size**.</span></span>  <span data-ttu-id="3d867-135">Размер cookie-файла (в байтах).</span><span class="sxs-lookup"><span data-stu-id="3d867-135">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="3d867-136">**Http**.</span><span class="sxs-lookup"><span data-stu-id="3d867-136">**HTTP**.</span></span>  <span data-ttu-id="3d867-137">Если значение равно true, это поле указывает на то, что файл cookie следует использовать только по протоколу HTTP и не может быть изменен на JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3d867-137">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="3d867-138">Просмотр [файлов cookie для HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="3d867-138">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="3d867-139">**Безопасность**.</span><span class="sxs-lookup"><span data-stu-id="3d867-139">**Secure**.</span></span>  <span data-ttu-id="3d867-140">Если значение равно true, это поле указывает на то, что файл cookie должен быть отправлен на сервер только через безопасное HTTPS-соединение.</span><span class="sxs-lookup"><span data-stu-id="3d867-140">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="3d867-141">Просмотр [защищенных файлов cookie][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="3d867-141">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="3d867-142">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="3d867-142">**SameSite**.</span></span>  <span data-ttu-id="3d867-143">Содержит `strict` или `lax` Если объект cookie использует экспериментальный атрибут [SameSite][MDNHTTPCookiesSamesite] .</span><span class="sxs-lookup"><span data-stu-id="3d867-143">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  

## <span data-ttu-id="3d867-144">Фильтрация файлов cookie</span><span class="sxs-lookup"><span data-stu-id="3d867-144">Filter cookies</span></span>   

<span data-ttu-id="3d867-145">Используйте текстовое поле " **Фильтр** " для фильтрации файлов cookie по **имени** или **значению**.</span><span class="sxs-lookup"><span data-stu-id="3d867-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="3d867-146">Фильтрация по другим полям не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3d867-146">Filtering by other fields is not supported.</span></span>  

> ##### <span data-ttu-id="3d867-147">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="3d867-147">Figure 3</span></span>  
> <span data-ttu-id="3d867-148">Фильтрация файлов cookie, которые не содержат текст</span><span class="sxs-lookup"><span data-stu-id="3d867-148">Filtering out any cookies that do not contain the text</span></span> `ID`  
> ![Фильтрация файлов cookie, которые не содержат идентификатор текста][ImageCookiesFilter]  

## <span data-ttu-id="3d867-150">Изменение файла cookie</span><span class="sxs-lookup"><span data-stu-id="3d867-150">Edit a cookie</span></span>   

<span data-ttu-id="3d867-151">Поля « **имя**», « **значение**», « **домен**», « **путь**» и « **срок действия/максимум»** можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="3d867-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="3d867-152">Дважды щелкните поле, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="3d867-152">Double-click a field to edit it.</span></span>  

> ##### <span data-ttu-id="3d867-153">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="3d867-153">Figure 4</span></span>  
> <span data-ttu-id="3d867-154">Установка имени файла cookie</span><span class="sxs-lookup"><span data-stu-id="3d867-154">Setting the name of a cookie to</span></span> `DEVTOOLS!`  
> ![Присвоение имени файла cookie DEVTOOLS!][ImageEditCookie]  

## <span data-ttu-id="3d867-156">Удаление файлов cookie</span><span class="sxs-lookup"><span data-stu-id="3d867-156">Delete cookies</span></span>   

<span data-ttu-id="3d867-157">Выберите нужный файл, а затем нажмите кнопку **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] , чтобы удалить один файл cookie.</span><span class="sxs-lookup"><span data-stu-id="3d867-157">Select a cookie and then click **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete that one cookie.</span></span>  

> ##### <span data-ttu-id="3d867-158">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="3d867-158">Figure 5</span></span>  
> <span data-ttu-id="3d867-159">Удаление определенного файла cookie</span><span class="sxs-lookup"><span data-stu-id="3d867-159">Deleting a specific cookie</span></span>  
> ![Удаление определенного файла cookie][ImageDeleteCookie]  

<span data-ttu-id="3d867-161">**Clear All** ![ ][ImageClearIcon] Чтобы удалить все файлы cookie, выберите Очистить все очистить все.</span><span class="sxs-lookup"><span data-stu-id="3d867-161">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

> ##### <span data-ttu-id="3d867-162">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="3d867-162">Figure 6</span></span>  
> <span data-ttu-id="3d867-163">Удаление всех файлов cookie</span><span class="sxs-lookup"><span data-stu-id="3d867-163">Clearing all cookies</span></span>  
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
> <span data-ttu-id="3d867-179">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3d867-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3d867-180">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3d867-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3d867-182">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3d867-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

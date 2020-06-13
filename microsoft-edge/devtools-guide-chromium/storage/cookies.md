---
title: Просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: ecd8df7058bca4535d1f7da15ce1d500ef85aefe
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710373"
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

# <span data-ttu-id="afb33-103">Просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="afb33-103">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="afb33-104">[Cookie-файлы HTTP][MDNHTTPCookies] преимущественно используются для управления сеансами пользователей, хранения параметров персонализации пользователей и отслеживания поведения пользователей.</span><span class="sxs-lookup"><span data-stu-id="afb33-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="afb33-105">Файлы cookie — это также причина, по которой на этой странице используются формы разрешения файлов cookie, которые вы видите в Интернете.</span><span class="sxs-lookup"><span data-stu-id="afb33-105">Cookies are also the cause of all of the annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="afb33-106">В приведенном ниже руководстве объясняется, как просматривать, изменять и удалять cookie-файлы HTTP для страницы с [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="afb33-106">The following guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="afb33-107">Открытие области "файлы cookie"</span><span class="sxs-lookup"><span data-stu-id="afb33-107">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="afb33-108">[Откройте DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="afb33-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="afb33-109">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="afb33-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="afb33-110">Откроется область **манифеста** .</span><span class="sxs-lookup"><span data-stu-id="afb33-110">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="afb33-112">Рисунок 1: область манифеста</span><span class="sxs-lookup"><span data-stu-id="afb33-112">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="afb33-113">В разделе **хранилище** разверните **cookie-файлы**, а затем выберите источник.</span><span class="sxs-lookup"><span data-stu-id="afb33-113">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Область «cookies»" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="afb33-115">Рисунок 2: область "cookie"</span><span class="sxs-lookup"><span data-stu-id="afb33-115">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <span data-ttu-id="afb33-116">Поля</span><span class="sxs-lookup"><span data-stu-id="afb33-116">Fields</span></span>  

<span data-ttu-id="afb33-117">Таблица **cookies** включает в себя указанные ниже поля.</span><span class="sxs-lookup"><span data-stu-id="afb33-117">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="afb33-118">**Имя**.</span><span class="sxs-lookup"><span data-stu-id="afb33-118">**Name**.</span></span>  <span data-ttu-id="afb33-119">Имя cookie-файла.</span><span class="sxs-lookup"><span data-stu-id="afb33-119">The name of the cookie.</span></span>  
*   <span data-ttu-id="afb33-120">**Value (значение**).</span><span class="sxs-lookup"><span data-stu-id="afb33-120">**Value**.</span></span>  <span data-ttu-id="afb33-121">Значение cookie-файла.</span><span class="sxs-lookup"><span data-stu-id="afb33-121">The value of the cookie.</span></span>  
*   <span data-ttu-id="afb33-122">**Domain (домен**).</span><span class="sxs-lookup"><span data-stu-id="afb33-122">**Domain**.</span></span>  <span data-ttu-id="afb33-123">Узлы, которым разрешено принимать cookie-файлы.</span><span class="sxs-lookup"><span data-stu-id="afb33-123">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="afb33-124">Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="afb33-124">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="afb33-125">**Path (путь**).</span><span class="sxs-lookup"><span data-stu-id="afb33-125">**Path**.</span></span>  <span data-ttu-id="afb33-126">URL-адрес, который должен существовать в запрашиваемом URL-адресе, чтобы отправить `Cookie` заголовок.</span><span class="sxs-lookup"><span data-stu-id="afb33-126">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="afb33-127">Ознакомьтесь [с областями cookie-файлов][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="afb33-127">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="afb33-128">**Истекает/Макс-возраст**.</span><span class="sxs-lookup"><span data-stu-id="afb33-128">**Expires / Max-Age**.</span></span>  <span data-ttu-id="afb33-129">Дата окончания срока действия или максимальный возраст cookie-файла.</span><span class="sxs-lookup"><span data-stu-id="afb33-129">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="afb33-130">Просмотр [постоянных файлов cookie][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="afb33-130">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="afb33-131">Для [cookie-файлов сеанса][MDNHTTPCookiesSession] это значение всегда `Session` .</span><span class="sxs-lookup"><span data-stu-id="afb33-131">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="afb33-132">**Размер**.</span><span class="sxs-lookup"><span data-stu-id="afb33-132">**Size**.</span></span>  <span data-ttu-id="afb33-133">Размер cookie-файла (в байтах).</span><span class="sxs-lookup"><span data-stu-id="afb33-133">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="afb33-134">**Http**.</span><span class="sxs-lookup"><span data-stu-id="afb33-134">**HTTP**.</span></span>  <span data-ttu-id="afb33-135">Если значение равно true, это поле указывает на то, что файл cookie следует использовать только по протоколу HTTP и не может быть изменен на JavaScript.</span><span class="sxs-lookup"><span data-stu-id="afb33-135">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="afb33-136">Просмотр [файлов cookie для HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="afb33-136">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="afb33-137">**Безопасность**.</span><span class="sxs-lookup"><span data-stu-id="afb33-137">**Secure**.</span></span>  <span data-ttu-id="afb33-138">Если значение равно true, это поле указывает на то, что файл cookie должен быть отправлен на сервер только через безопасное HTTPS-соединение.</span><span class="sxs-lookup"><span data-stu-id="afb33-138">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="afb33-139">Просмотр [защищенных файлов cookie][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="afb33-139">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="afb33-140">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="afb33-140">**SameSite**.</span></span>  <span data-ttu-id="afb33-141">Содержит `strict` или `lax` Если объект cookie использует экспериментальный атрибут [SameSite][MDNHTTPCookiesSamesite] .</span><span class="sxs-lookup"><span data-stu-id="afb33-141">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="afb33-142">**Priority (приоритет**).</span><span class="sxs-lookup"><span data-stu-id="afb33-142">**Priority**.</span></span>  <span data-ttu-id="afb33-143">Contains `low` , `medium` \ (по умолчанию \) или, `high` Если cookie использует устаревший атрибут [приоритета cookie-файлов][ChromiumIssue232693] .</span><span class="sxs-lookup"><span data-stu-id="afb33-143">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <span data-ttu-id="afb33-144">Фильтрация файлов cookie</span><span class="sxs-lookup"><span data-stu-id="afb33-144">Filter cookies</span></span>  

<span data-ttu-id="afb33-145">Используйте текстовое поле " **Фильтр** " для фильтрации файлов cookie по **имени** или **значению**.</span><span class="sxs-lookup"><span data-stu-id="afb33-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="afb33-146">Фильтрация по другим полям не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="afb33-146">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Фильтрация файлов cookie, которые не содержат идентификатор текста" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="afb33-148">Рис. 3: Фильтрация файлов cookie, которые не содержат текст</span><span class="sxs-lookup"><span data-stu-id="afb33-148">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <span data-ttu-id="afb33-149">Изменение файла cookie</span><span class="sxs-lookup"><span data-stu-id="afb33-149">Edit a cookie</span></span>  

<span data-ttu-id="afb33-150">Поля « **имя**», « **значение**», « **домен**», « **путь**» и « **срок действия/максимум»** можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="afb33-150">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="afb33-151">Дважды щелкните поле, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="afb33-151">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Присвоение имени файла cookie DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="afb33-153">Рисунок 4: Задание имени файла cookie</span><span class="sxs-lookup"><span data-stu-id="afb33-153">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <span data-ttu-id="afb33-154">Удаление файлов cookie</span><span class="sxs-lookup"><span data-stu-id="afb33-154">Delete cookies</span></span>  

<span data-ttu-id="afb33-155">Выберите файл cookie и выберите пункт **Удалить выбранное** ![ удаление, ][ImageDeleteIcon] чтобы удалить определенный файл cookie.</span><span class="sxs-lookup"><span data-stu-id="afb33-155">Select a cookie and select **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Удаление определенного файла cookie" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="afb33-157">Рисунок 5: удаление определенного файла cookie</span><span class="sxs-lookup"><span data-stu-id="afb33-157">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="afb33-158">**Clear All** ![ ][ImageClearIcon] Чтобы удалить все файлы cookie, выберите Очистить все очистить все.</span><span class="sxs-lookup"><span data-stu-id="afb33-158">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Удаление всех файлов cookie" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="afb33-160">Рисунок 6: Очистка всех cookie-файлов</span><span class="sxs-lookup"><span data-stu-id="afb33-160">Figure 6:  Clearing all cookies</span></span>  
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
> <span data-ttu-id="afb33-170">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="afb33-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="afb33-171">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="afb33-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="afb33-173">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="afb33-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

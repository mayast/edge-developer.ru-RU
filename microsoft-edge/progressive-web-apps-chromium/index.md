---
description: Прогрессивные веб-приложения работают с родными в Windows 10.  Вот все, что вам нужно знать как веб-разработчик.
title: Прогрессивные веб-приложения для Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, EDGE, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 482f498e246ee265424f7b80ff3cd67f78501ee2
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583037"
---
# <span data-ttu-id="f5a2a-105">Прогрессивные веб-приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="f5a2a-105">Progressive Web Apps on Windows</span></span>  

<span data-ttu-id="f5a2a-106">С помощью [последовательного веб-приложения][MDNApps] \ (или просто PWAs \) вам не нужно определять использование открытых веб-технологий для взаимодействия между платформами и предоставление пользователям собственного приложения, такого как приложение, настроенное для своих устройств.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-106">With [Progressive Web Apps][MDNApps] \(or simply PWAs\), you do not have to decide between using open web technologies for cross-platform interoperability and providing your users with a native app-like experience customized for their devices.</span></span>  <span data-ttu-id="f5a2a-107">PWAs — это только веб-сайты, которые [последовательно расширены][AListApartUnderstandingProgressiveEnhancement] для работы, например собственные приложения на поддерживаемых платформах.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-107">PWAs are just websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="f5a2a-108">В приложениях PWA объединены лучшие качестве веб- и собственных приложения.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        ![Значок с возможностью обнаружения][ImageISearch]
        ### [<span data-ttu-id="f5a2a-110">Обнаруживаемым</span><span class="sxs-lookup"><span data-stu-id="f5a2a-110">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="f5a2a-111">Из результатов поиска в Интернете и поддержки магазинов приложений</span><span class="sxs-lookup"><span data-stu-id="f5a2a-111">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        ![Устанавливаемый значок][ImageIPackage]
        ### [<span data-ttu-id="f5a2a-113">Устанавливаемый</span><span class="sxs-lookup"><span data-stu-id="f5a2a-113">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="f5a2a-114">Закрепление и запуск на начальном экране, меню "Пуск", панели задач и т. д.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-114">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        ![Значок повторного запуска][ImageIPushNotification]
        ### [<span data-ttu-id="f5a2a-116">Повторное участие</span><span class="sxs-lookup"><span data-stu-id="f5a2a-116">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="f5a2a-117">Отправлять push-уведомления, даже если приложение неактивно</span><span class="sxs-lookup"><span data-stu-id="f5a2a-117">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
    :::column:::
        ![Значок, не зависящий от сети][ImageIOffline]
        ### [<span data-ttu-id="f5a2a-119">Сетевая независимость</span><span class="sxs-lookup"><span data-stu-id="f5a2a-119">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="f5a2a-120">Работа в автономном режиме и в условиях низкой сети</span><span class="sxs-lookup"><span data-stu-id="f5a2a-120">Works offline and in low-network conditions</span></span>
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Значок прогрессивной развертки][ImageIProgressive]
        ### [<span data-ttu-id="f5a2a-122">JPEG</span><span class="sxs-lookup"><span data-stu-id="f5a2a-122">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="f5a2a-123">Работа с возможностями устройства в масштабе (или в меньшую сторону)</span><span class="sxs-lookup"><span data-stu-id="f5a2a-123">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        ![Значок "безопасный"][ImageISecurity]
        ### [<span data-ttu-id="f5a2a-125">Безопасной</span><span class="sxs-lookup"><span data-stu-id="f5a2a-125">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="f5a2a-126">Обеспечивает защищенную конечную точку HTTPS и другие меры для защиты от пользователей</span><span class="sxs-lookup"><span data-stu-id="f5a2a-126">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
    :::column:::
        ![Значок отклика][ImageIResponsive]
        ### [<span data-ttu-id="f5a2a-128">Хорошая скорость отклика</span><span class="sxs-lookup"><span data-stu-id="f5a2a-128">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="f5a2a-129">Адаптируется к размеру экрана или ориентации и методу ввода для пользователя</span><span class="sxs-lookup"><span data-stu-id="f5a2a-129">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        ![Значок ссылки][ImageILink]
        ### [<span data-ttu-id="f5a2a-131">Связь</span><span class="sxs-lookup"><span data-stu-id="f5a2a-131">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="f5a2a-132">Предоставление общего доступа к файлу и его запуск с помощью стандартной гиперссылки</span><span class="sxs-lookup"><span data-stu-id="f5a2a-132">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="f5a2a-133">Создав или преобразуя существующий веб-сайт в PWA, вы приносите к ним более эффективное использование push-уведомлений, интеграция с приложением и поддержку в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-133">By building or converting your existing site to a PWA, you engage better with your existing audience using push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="f5a2a-134">В то же время вы должны продолжать собирать аудиторию в открытом веб-браузере, так как пользователи могут найти ваше приложение PWA с помощью поиска и совместного использования ссылок.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-134">At the same time, you should continue to build your audience on the open web, as users discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="f5a2a-135">Вы можете обновить свое приложение, просто обновив код веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-135">Best of all, you may update your app by simply updating your web server code.</span></span>  

## <span data-ttu-id="f5a2a-136">PWAs в Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="f5a2a-136">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="f5a2a-137">При создании последовательного веб-приложения, нацеленного на веб-интерфейс API, приложение может быть развернуто на разных платформах и устройствах, а также доступны специальные возможности устройства, доступные для использования.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-137">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device specific capabilities as available.</span></span>  <span data-ttu-id="f5a2a-138">PWAs в Microsoft Edge \ (Chromium \) являются полностью стандартными на основе веб-платформы и позволяют пользователям устанавливать приложение прямо из браузера, не требуя наличия развертывания и регистрации на основе магазина.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-138">PWAs in Microsoft Edge \(Chromium\) are completely standards-based from a web platform perspective and enable users to install the app directly from within the browser without the need for Store-based deployment or registration.</span></span>  <span data-ttu-id="f5a2a-139">Классическое PWAs поддерживается на любой из платформ Microsoft Edge \ (Chromium \), включая Windows 7, Windows 10 и macOS.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-139">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available, including Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="f5a2a-140">К другим преимуществам относятся:</span><span class="sxs-lookup"><span data-stu-id="f5a2a-140">Other benefits include:</span></span>  

*   <span data-ttu-id="f5a2a-141">Приложения можно устанавливать прямо из браузера с помощью значка **установки** на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-141">Applications may be installed directly from within the browser via the **Install** icon in the navigation bar.</span></span>  
    
    ![Всплывающее меню и значок установки приложения][ImageInstallPwa]  
    
*   <span data-ttu-id="f5a2a-143">Приложения также могут быть установлены, запущены и обрабатываются в меню " **Параметры**  >  **Apps** "</span><span class="sxs-lookup"><span data-stu-id="f5a2a-143">Applications may also be installed, run and managed from the **Settings** > **Apps** menu</span></span>  
    
    ![Элементы меню "приложение" в разделе "Параметры"][ImageAppMenus]  

*   <span data-ttu-id="f5a2a-145">Веб-уведомления интегрированы в систему уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="f5a2a-145">Web Notifications are integrated into the Windows notification system</span></span>
*   <span data-ttu-id="f5a2a-146">Общее хранилище файлов cookie с профилем браузера, в котором установлено приложение</span><span class="sxs-lookup"><span data-stu-id="f5a2a-146">Shared cookie store with the browser profile that installed the app</span></span>
*   <span data-ttu-id="f5a2a-147">Доступ к другим функциям браузера через `...` меню, включая проверку сертификата, разрешения сайтов, защиту от слежения и расширения браузера.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-147">Access to other browser features via the `...` menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>
*   <span data-ttu-id="f5a2a-148">Полный доступ к [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] для отладки приложения</span><span class="sxs-lookup"><span data-stu-id="f5a2a-148">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f5a2a-149">Чтобы настроить PWAs специально для Windows 10, которые делают запросы API WinRT с помощью JavaScript, ознакомьтесь с [документацией, относящейся к функциям EDGEHTML PWA][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="f5a2a-149">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, see the [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="f5a2a-150">Узнайте больше о том, как тестировать PWA в Windows 10 и распространять его в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-150">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

## <span data-ttu-id="f5a2a-151">Требования</span><span class="sxs-lookup"><span data-stu-id="f5a2a-151">Requirements</span></span>  

<span data-ttu-id="f5a2a-152">Для работы в качестве PWA веб-приложение, размещенное на сервере, должно включать следующие минимальные требования.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

|  | <span data-ttu-id="f5a2a-153">Требование</span><span class="sxs-lookup"><span data-stu-id="f5a2a-153">Requirement</span></span> | <span data-ttu-id="f5a2a-154">Сведения</span><span class="sxs-lookup"><span data-stu-id="f5a2a-154">Details</span></span> | 
|:--- |:--- |:--- |  
| <span data-ttu-id="f5a2a-155">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-155">X</span></span> | [<span data-ttu-id="f5a2a-156">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f5a2a-156">HTTPS</span></span>][WikiHttps] | <span data-ttu-id="f5a2a-157">Защитите своих пользователей, обеспечив надежную связь с сервером или приложением.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-157">Protect your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="f5a2a-158">Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемыми в безопасном соединении (или в `localhost` целях отладки).</span><span class="sxs-lookup"><span data-stu-id="f5a2a-158">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  |  
| <span data-ttu-id="f5a2a-159">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-159">X</span></span> | [<span data-ttu-id="f5a2a-160">Обслуживание сотрудников</span><span class="sxs-lookup"><span data-stu-id="f5a2a-160">Service Workers</span></span>][MDNServiceWorkerApi] | <span data-ttu-id="f5a2a-161">Используйте рабочие потоки служб, чтобы выступать в качестве сетевых прокси между сервером и клиентским приложением, чтобы обеспечить поддержку в автономном режиме, кэшировании ресурсов, push-уведомлениях, фоновой синхронизации данных и оптимизации производительности загрузки страниц.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-161">Use Service Worker threads to act as network proxies between your server and client app in order to provide offline support, resource caching, push notifications, background data sync, and  page load perf optimizations.</span></span>  |  
| <span data-ttu-id="f5a2a-162">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-162">X</span></span> | [<span data-ttu-id="f5a2a-163">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f5a2a-163">Web App Manifest</span></span>][MDNWebAppManifest] | <span data-ttu-id="f5a2a-164">Предоставьте файл метаданных на основе JSON, описывающий ключевые сведения о вашем веб-приложении, (например, значки, язык и точку входа URL \), поэтому Windows 10 и другие платформы узла смогут предоставлять пользователям PWA доступ к устанавливаемому исходному приложению.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-164">Provide a JSON-based metadata file describing key information about your web app \(such as icons, language, and URL entry point\), so that Windows 10 and other host platforms are able to provide your PWA users with an installable, native app-like experience.</span></span>  |  

<span data-ttu-id="f5a2a-165">Для того чтобы стать прекрасным PWA, ваше приложение должно также отвечать указанным ниже требованиям.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-165">To be a great PWA, your app must also meet the following requirements.</span></span>  

|  | <span data-ttu-id="f5a2a-166">Требование</span><span class="sxs-lookup"><span data-stu-id="f5a2a-166">Requirement</span></span> | <span data-ttu-id="f5a2a-167">Сведения</span><span class="sxs-lookup"><span data-stu-id="f5a2a-167">Details</span></span> | 
|:--- |:--- |:--- |  
| <span data-ttu-id="f5a2a-168">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-168">X</span></span> | [<span data-ttu-id="f5a2a-169">Совместимость с различными браузерами</span><span class="sxs-lookup"><span data-stu-id="f5a2a-169">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting] | <span data-ttu-id="f5a2a-170">Убедитесь, что веб-приложение PWA [работает в разных][MicrosoftDeveloperEdgeToolsRemote] браузерах и средах.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-170">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  |  
| <span data-ttu-id="f5a2a-171">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-171">X</span></span> | [<span data-ttu-id="f5a2a-172">Адаптивный дизайн</span><span class="sxs-lookup"><span data-stu-id="f5a2a-172">Responsive design</span></span>][WikiResponsiveWebDesign] | <span data-ttu-id="f5a2a-173">Использование жидкостных макетов и гибких изображений с помощью [сетки][MDNCssGridLayout]CSS, [гибкого бокса][MDNCssFlexibleBoxLayout], [сетки][MDNCssGridLayout] CSS и гибкого [бокса][MDNCssFlexibleBoxLayout] , [мультимедийных запросов][MDNMediaQueries]и [отклика изображений][MDNResponsiveImages] для адаптации вашего UX к устройству пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-173">Employ fluid layouts and flexible images with CSS [grid][MDNCssGridLayout], [flexbox][MDNCssFlexibleBoxLayout], CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout] , [media queries][MDNMediaQueries], and [responsive images][MDNResponsiveImages] to adapt your UX to your user's device.</span></span>  <span data-ttu-id="f5a2a-174">Используйте [средства эмуляции устройства][DevToolsGuide|::ref1::|] в браузере для проверки на локальном компьютере или настройте [сеанс удаленной отладки][DevToolsProtocolClientsEdgeDevToolsPreview] для проверки непосредственно на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-174">Use [device emulation tools][DevToolsGuide|::ref1::|] from your browser to test locally, or set up a [remote debugging session][DevToolsProtocolClientsEdgeDevToolsPreview] to test directly on a target device.</span></span>  |  
| <span data-ttu-id="f5a2a-175">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-175">X</span></span> | [<span data-ttu-id="f5a2a-176">Глубокая связь</span><span class="sxs-lookup"><span data-stu-id="f5a2a-176">Deep linking</span></span>][WikiDeepLinking] | <span data-ttu-id="f5a2a-177">Перенаправление каждой страницы сайта на уникальный URL-адрес, чтобы пользователи могли пользоваться более широкой аудиторией через функцию совместного использования социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-177">Route each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  |  
| <span data-ttu-id="f5a2a-178">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-178">X</span></span> | [<span data-ttu-id="f5a2a-179">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="f5a2a-179">Best practices</span></span>][Webhint] | <span data-ttu-id="f5a2a-180">Используйте средства качества кода, такие как Linter веб – [Подсказка][Webhint] , чтобы оптимизировать эффективность, надежность, безопасность и доступность вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-180">Use code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  |  
| <span data-ttu-id="f5a2a-181">X</span><span class="sxs-lookup"><span data-stu-id="f5a2a-181">X</span></span> | [<span data-ttu-id="f5a2a-182">Контрольный список для Chromium PWA</span><span class="sxs-lookup"><span data-stu-id="f5a2a-182">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist] | <span data-ttu-id="f5a2a-183">Убедитесь, что у PWA есть контрольный список Google Baseline PWA.</span><span class="sxs-lookup"><span data-stu-id="f5a2a-183">Check your PWA against the Google baseline PWA checklist.</span></span>  |  

<span data-ttu-id="f5a2a-184">Если вы хотите преобразовать PWA в приложение [Microsoft Store][MicrosoftDeveloperStore] , заголовков, посвященных [последовательной документации на веб-приложения (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .</span><span class="sxs-lookup"><span data-stu-id="f5a2a-184">If you want to turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, head to the [Progressive Web Apps (EdgeHTML)][PwaEdgehtmlMicrosoftStore] documentation.</span></span>  

## <span data-ttu-id="f5a2a-185">Текущая доступность</span><span class="sxs-lookup"><span data-stu-id="f5a2a-185">Current availability</span></span>  

<span data-ttu-id="f5a2a-186">Поддержка обработчиком прогрессивных веб-приложений запросов на некоторые архитектурные компоненты — наиболее существенная сетевая инфраструктура, базовая для [API выборки][MDNFetchApi].</span><span class="sxs-lookup"><span data-stu-id="f5a2a-186">Browser engine support for Progressive Web App requests for a number of architectural components, the most significant being the networking infrastructure underlying the [Fetch API][MDNFetchApi].</span></span>  

<span data-ttu-id="f5a2a-187">Для Microsoft Edge \ (Chromium \) веб-платформа включает полную поддержку этих функций, которые работают на разных устройствах, где поддерживается Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="f5a2a-187">For Microsoft Edge \(Chromium\), the browser platform includes full support for these features that work across devices where Microsoft Edge \(Chromium\) is supported.</span></span>  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

[ImageInstallPwa]: ./media/Install_PWA.png  
[ImageAppMenus]: ./media/App_menus.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Клиенты Microsoft Edge DevTools Preview-DevTools Protocol"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Эмуляции"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps.md "Отладка последовательного веб-приложения"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Новые возможности EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Новые возможности EdgeHTML 14"  
[PwaEdgehtmlIndex]: ../progressive-web-apps-edgehtml/index.md "Прогрессивные веб-приложения (EdgeHTML) в Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Прогрессивные веб-приложения в Microsoft Store"
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Общие сведения о службах push-уведомлений Windows \ (WNS \)"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Проектирование для Xbox и телевизора"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Вопросы пользовательского интерфейса для устройств UWP"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Что такое приложение универсальной платформы Windows (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Поддержка приложения с помощью фоновых задач"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Публикация приложений и игр для Windows"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Открытие учетной записи разработчика"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Welcoming последовательного веб-приложения в Microsoft EDGE и Windows 10 — блоги Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API фоновой синхронизации — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Манифест веб-приложения — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Мгновенное Тестирование"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Смешанная реальность для разработчиков"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface HUB"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Магазин Microsoft Developer"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Скачать новый браузер Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Включение и отключение фокусной помощи в Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Изменение параметров уведомлений в Windows 10"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Раскрывающийся список "последовательное расширение""  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "приложения | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Тестирование нескольких браузеров | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Макет гибких полей CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Получить API | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Запросы мультимедиа | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Возможности, которые могут быть обнаружены последовательностью веб-приложения"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Преимущества устанавливаемого веб-приложения с прогрессивным управлением"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Преимущества веб-приложений, поддерживающих связь"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Преимущества независимых от сети веб-приложений"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Преимущества последовательного веб-приложения"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Повторное подключение к веб-приложениям с последовательной подобщением"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Преимущества использования веб-приложения с откликом"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Преимущества надежного веб-приложения"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Изображения с откликом | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочего процесса службы | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Что делает подходящее прогрессивное веб-приложение? | Web. dev"  

[Webhint]: https://webhint.io "Подсказка"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Глубокая связь — Википедии"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Википедии"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Отклики на веб-дизайн — Википедии"  

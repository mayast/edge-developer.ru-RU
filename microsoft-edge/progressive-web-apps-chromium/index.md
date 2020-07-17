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
ms.openlocfilehash: 90740bac07ebfd74f89e2524e6955621e1b09b05
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882809"
---
# Прогрессивные веб-приложения для Windows  

С помощью [последовательного веб-приложения][MDNApps] \ (или просто PWAs \) вам не нужно определять использование открытых веб-технологий для взаимодействия между платформами и предоставление пользователям собственного приложения, такого как приложение, настроенное для своих устройств.  PWAs — это только веб-сайты, которые [последовательно расширены][AListApartUnderstandingProgressiveEnhancement] для работы, например собственные приложения на поддерживаемых платформах.  В приложениях PWA объединены лучшие качестве веб- и собственных приложения.  

:::row:::
    :::column:::
        ![Значок с возможностью обнаружения][ImageISearch]
        ### [Обнаруживаемым][MDNPwaAdvantagesDiscoverable]
        Из результатов поиска в Интернете и поддержки магазинов приложений
    :::column-end:::
    :::column:::
        ![Устанавливаемый значок][ImageIPackage]
        ### [Устанавливаемый][MDNPwaAdvantagesInstallable]
        Закрепление и запуск на начальном экране, меню "Пуск", панели задач и т. д.
    :::column-end:::
    :::column:::
        ![Значок повторного запуска][ImageIPushNotification]
        ### [Повторное участие][MDNPwaAdvantagesReEngageable]
        Отправлять push-уведомления, даже если приложение неактивно
    :::column-end:::
    :::column:::
        ![Значок, не зависящий от сети][ImageIOffline]
        ### [Сетевая независимость][MDNPwaAdvantagesNetworkIndependent]
        Работа в автономном режиме и в условиях низкой сети
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Значок прогрессивной развертки][ImageIProgressive]
        ### [JPEG][MDNPwaAdvantagesProgressive]
        Работа с возможностями устройства в масштабе (или в меньшую сторону)
    :::column-end:::
    :::column:::
        ![Значок "безопасный"][ImageISecurity]
        ### [Безопасной][MDNPwaAdvantagesSafe]
        Обеспечивает защищенную конечную точку HTTPS и другие меры для защиты от пользователей
    :::column-end:::
    :::column:::
        ![Значок отклика][ImageIResponsive]
        ### [Хорошая скорость отклика][MDNPwaAdvantagesResponsive]
        Адаптируется к размеру экрана или ориентации и методу ввода для пользователя
    :::column-end:::
    :::column:::
        ![Значок ссылки][ImageILink]
        ### [Связь][MDNPwaAdvantagesLinkable]
        Предоставление общего доступа к файлу и его запуск с помощью стандартной гиперссылки
    :::column-end:::
:::row-end:::

Создав или преобразуя существующий веб-сайт в PWA, вы приносите к ним более эффективное использование push-уведомлений, интеграция с приложением и поддержку в автономном режиме.  В то же время вы должны продолжать собирать аудиторию в открытом веб-браузере, так как пользователи могут найти ваше приложение PWA с помощью поиска и совместного использования ссылок.  Вы можете обновить свое приложение, просто обновив код веб-сервера.  

## PWAs в Microsoft EDGE (Chromium)  

При создании последовательного веб-приложения, нацеленного на веб-интерфейс API, приложение может быть развернуто на разных платформах и устройствах, а также доступны специальные возможности устройства, доступные для использования.  PWAs в Microsoft Edge \ (Chromium \) являются полностью стандартными на основе веб-платформы и позволяют пользователям устанавливать приложение прямо из браузера, не требуя наличия развертывания и регистрации на основе магазина.  Классическое PWAs поддерживается на любой из платформ Microsoft Edge \ (Chromium \), включая Windows 7, Windows 10 и macOS.  К другим преимуществам относятся:  

*   Приложения можно устанавливать прямо из браузера с помощью значка **установки** на панели навигации.  
    
    ![Всплывающее меню и значок установки приложения][ImageInstallPwa]  
    
*   Приложения также могут быть установлены, запущены и обрабатываются в меню " **Параметры**  >  **Apps** "  
    
    ![Элементы меню "приложение" в разделе "Параметры"][ImageAppMenus]  

*   Веб-уведомления интегрированы в систему уведомлений Windows
*   Общее хранилище файлов cookie с профилем браузера, в котором установлено приложение
*   Доступ к другим функциям браузера через `...` меню, включая проверку сертификата, разрешения сайтов, защиту от слежения и расширения браузера.
*   Полный доступ к [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] для отладки приложения  

> [!IMPORTANT]
> Чтобы настроить PWAs специально для Windows 10, которые делают запросы API WinRT с помощью JavaScript, ознакомьтесь с [документацией, относящейся к функциям EDGEHTML PWA][PwaEdgehtmlIndex].  Узнайте больше о том, как тестировать PWA в Windows 10 и распространять его в Microsoft Store.  

> [!NOTE]
> В [сеансе сборки 2020 PWA][BuildVideo] вы можете найти общие сведения о преимуществах PWA, предстоящих функциях и кратких видеодемонстрациях. 

## Требования  

Для работы в качестве PWA веб-приложение, размещенное на сервере, должно включать следующие минимальные требования.  

| Требование | Сведения | 
|:--- |:--- |  
| [HTTPS][WikiHttps] | Защитите своих пользователей, обеспечив надежную связь с сервером или приложением.  Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемыми в безопасном соединении (или в `localhost` целях отладки).  |  
| [Служебные сценарии][MDNServiceWorkerApi] | Используйте рабочие потоки служб, чтобы выступать в качестве сетевых прокси между сервером и клиентским приложением, чтобы обеспечить поддержку в автономном режиме, кэшировании ресурсов, push-уведомлениях, фоновой синхронизации данных и оптимизации производительности загрузки страниц.  |  
| [Манифест веб-приложения][MDNWebAppManifest] | Предоставьте файл метаданных на основе JSON, описывающий ключевые сведения о вашем веб-приложении, (например, значки, язык и точку входа URL \), поэтому Windows 10 и другие платформы узла смогут предоставлять пользователям PWA доступ к устанавливаемому исходному приложению.  |  

Для того чтобы стать прекрасным PWA, ваше приложение должно также отвечать указанным ниже требованиям.  

| Требование | Сведения | 
|:--- |:--- |  
| [Совместимость с различными браузерами][MDNCrossBrowserTesting] | Убедитесь, что веб-приложение PWA [работает в разных][MicrosoftDeveloperEdgeToolsRemote] браузерах и средах.  |  
| [Адаптивный дизайн][WikiResponsiveWebDesign] | Использование жидкостных макетов и гибких изображений с помощью [сетки][MDNCssGridLayout]CSS, [гибкого бокса][MDNCssFlexibleBoxLayout], [сетки][MDNCssGridLayout] CSS и гибкого [бокса][MDNCssFlexibleBoxLayout] , [мультимедийных запросов][MDNMediaQueries]и [отклика изображений][MDNResponsiveImages] для адаптации вашего UX к устройству пользователя.  Используйте [средства эмуляции устройства][DevToolsGuide|::ref1::|] в браузере для проверки на локальном компьютере или настройте [сеанс удаленной отладки][DevToolsProtocolClientsEdgeDevToolsPreview] для проверки непосредственно на целевом устройстве.  |  
| [Глубокая связь][WikiDeepLinking] | Перенаправление каждой страницы сайта на уникальный URL-адрес, чтобы пользователи могли пользоваться более широкой аудиторией через функцию совместного использования социальных сетей.  |  
| [Рекомендации][Webhint] | Используйте средства качества кода, такие как Linter веб – [Подсказка][Webhint] , чтобы оптимизировать эффективность, надежность, безопасность и доступность вашего приложения.  |  
| [Контрольный список для Chromium PWA][WebDevGoodPwaChecklist] | Убедитесь, что у PWA есть контрольный список Google Baseline PWA.  |  

Если вы хотите преобразовать PWA в приложение [Microsoft Store][MicrosoftDeveloperStore] , заголовков, посвященных [последовательной документации на веб-приложения (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .  
  

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

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Предварительный просмотр Средств разработчика в Microsoft Edge — Клиенты протокола средств разработчика"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Эмуляция"  
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

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Видео PWA"

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Что делает подходящее прогрессивное веб-приложение? | Web. dev"  

[Webhint]: https://webhint.io "Подсказка"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Глубокая связь — Википедии"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Википедии"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Отклики на веб-дизайн — Википедии"  
